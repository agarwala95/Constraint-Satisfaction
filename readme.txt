Problem 1.2 Constraint Satisfaction

Question: 

	It is the night before Christmas and you are in the only shop in Munich still open. You still need to
	buy presents for your Mum, your Brother, your Grandma, your Grandpa, your Cousin, your Aunt, your
	Uncle, and your Significant Other. In the shop there are:
	-Dave Brubeck CDs, costing e10
	-Luxury Christmas socks, costing e7
	-Boxes of chocolates, costing e4
	-Coffee mills, costing e12
	Consider the following constraints:
	1. Each person must get exactly one present
	2. You have a total budget of e52
	3. Your mum, brother, and significant other must get different presents
	4. Your uncle and cousin must get different presents
	5. Your grandparents must get different presents
	6. Your mum and uncle must get different presents
	7. You cannot get chocolates for your mum, brother, significant other, or grandpa
	8. Your cousin must not get socks
	9. There is only one coffee mill in the shop
	10. There are no more than 2 CDs in the shop
	11. There are no more than 4 boxes of chocolates in the shop
	12. Your brother must get a CD
	13. Nobody gets chocolates
	Model the constraint satisfaction problem in Savile Row. For each of the following subsets of constraints,
	Find the solution, if it exists:
	Problem 1.1: {1-12}
	Problem 1.2: {1-3, 6-13}
	Problem 1.3: {1, 8-13}
	Problem 1.4: {1, 3-9, 11-13}
	Problem 1.5: {1, 3-12}

Solution:

	I find a 8 x 4 matrix that contains either 0,1 as values. I have made the table as:	
						CD	Socks	Chocolate	Coffee Mills
	Mum				
	Brother				
	Grandma				
	Grandpa				
	Cousin				
	Aunt				
	Uncle				
	Significant Other				

	Now a 1 in the 1st column and 1st cell means that Mum gets a CD. Similarly if 1 is assigned to the 3rd row and 2nd column then, Grandma gets a Socks.
	Using this logic, I have generated the following solutions:
	Solution 1.1:
	#Using Constraints 1-12
	No Solution

	Solution 1.2:
	#Using Constraints 1-3, 6-13
	No Solution

	Solution 1.3:
	#Using Constraints 1,8-13
	Mum	: Socks		
	Brother	: CD		
	Grandma	: CD		
	Grandpa	: Socks	
	Cousin : Coffee Mill
	Aunt : Socks
	Uncle : Socks			
	Significant Other : Socks

	Solution 1.4:
	#Using Constraints 1,3-9,11-13
	Mum	: Coffee Mill		
	Brother	: CD		
	Grandma	: CD	
	Grandpa	: Socks
	Cousin : CD	
	Aunt : Socks
	Uncle : Socks		
	Significant Other : Socks

	Solution 1.5:
	#Using Constraints 1,3-12
	Mum	: Socks		
	Brother	: CD		
	Grandma	: Chocolate	
	Grandpa	: Socks
	Cousin : Chocolate
	Aunt : Socks
	Uncle : CD		
	Significant Other : Coffee Mill
