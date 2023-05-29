<div align = "center"> 
   
# Desicion making  support analysis - Instituto Tecnológico y de Estudios Superiores de Monterrey
<div align = "left"> 

# Collaborative activity: Mini case 1 - Linear programming - Group 351
- María Fernanda Frías Carranza 
- Ana Sofía Ordaz Infansón	
- Sarahí Gómez Montiel	
- Ricardo Yael Carmona Zilli	 
- Jeniffer López Vilchis	
# Question set

Consider the WhiskasModel1.py

#### 1. What are the two parameters that the LpProblem function implements?
“Chicken percent” and “Beef percent”

#### 2. Is it mandatory to name thr prob variable as prob?
Is not mandatory to the the variable as prob, since a variable is a set of characters that can be assigned a value, you can assign any name to this variable. However, it is advisable to assign it a recognizable name that is associated with the format.

#### 3. What are LpContinous and LpInteger used for?
LpContinuous refers to continuous variables, any real value, integer and fractional values are considered, on the other hand LpInteger is for integer values, discrete numbers, without decimal values, where the answer has no fractional values. 

#### 4. Explain and copy the section of code that defines the objective function.
$The$ $objective$ $function$ $is$ $added$ $to$ $'prob'$ $first$

prob += 0.013 * x1 + 0.008 * x2, "Total Cost of Ingredients per can"
   
- prob +=: Shorthand for adding a new term to the problem.
- 40.013*x1 + 0.008*x2 : The mathematical expression that represents the total cost of Ingredients per can. It is a linear combination of two variables, ´x1´and ´x2´, multiplied by their respective coefficients (0.013 and 0.008). And these coefficients represent the cost per unit of each ingredient. 
- Total Cost of Ingredients per can : The name or label given to the objective function. It is a descriptive string that helps identify the objective function when running or analyzing the problem.
   
The objective function aims to minimize the total cost of ingredients per can by finding appropriate values for the variables ´x1´and ´x2´(representing the percentages of chicken and beef) while considering their associated costs


#### 5. Explain and copy the section of code that defines the constraints.
$The$ $five$ $constraints$ $are$ $entered$ 

prob += x1 + x2 == 100, "PercentagesSum"
   
prob += 0.100 * x1 + 0.200 * x2 >= 8.0, "ProteinRequirement"
   
prob += 0.080 * x1 + 0.100 * x2 >= 6.0, "FatRequirement"
   
prob += 0.001 * x1 + 0.005 * x2 <= 2.0, "FibreRequirement"
                                      
prob += 0.002 * x1 + 0.005 * x2 <= 0.4, "SaltRequirement"
- prob += x1 + x2 == 100, "PercentagesSum" ´ : It sets a constraint that the sum of ´x1´and ´x2´should be equal to 100. This ensures that the percentages of the ingredients (chicken and beef) add up to a total of 100%.
- ´ prob += 0.100*x1 + 0.200*x2 >= 8.0, "ProteinRequirement" ´: It sets a constraint related to the protein requirement. It indicates that the protein content, calculated as 0.100 multiplied by  ´x1´ (percentage of chicken) plus 0.200 multiplied by  ´x2´ (percentage of beef), must be greater than or equal to 8.0  .
- ´ prob += 0.080*x1 + 0.100*x2 >= 6.0, "FatRequirement" ´: It sets a constraint related to the fat requirement. It indicates that the fat content, calculated as 0.080  multiplied by  ´x1´ (percentage of chicken) plus 0.100 multiplied by  ´x2´ (percentage of beef), should be greater than or equal to 6.0  .
- ´ prob += 0.001*x1 + 0.005*x2 <= 2.0, "FiberRequirement" ´ : It sets a constraint related to the fiber requirement. It indicates that the fiber content, calculated as 0.001  multiplied by  ´x1´ (percentage of chicken) plus 0.005 multiplied by  ´x2´ (percentage of beef), should be less than or equal to 2.0  .
- ´ prob += 0.002*x1 + 0.005*x2 <= 0.4, "SaltRequirement" ´ :  It sets a constraint related to the salt requirement. It indicates that the salt content, calculated as 0.002  multiplied by  ´x1´ (percentage of chicken) plus 0.005 multiplied by  ´x2´ (percentage of beef), should be less than or equal to 0.4.
   
   
These constraints ensure that the ingredient percentages meet the total sum, protein, fat, fiber and salt requirements specified in the problem.


#### 6. Is this a minimization or maximization problem?
Minimization

#### 7. Run the WhiskasModel1.py code. (no need to make changes, just runt it as is) What is the value of the following variables.
- Status:
   BeefPercent = 66.67%
   ChickenPercent = 33.33%
   Total Cost of Ingredients per can = .96 cents per can
 - Status Full Formulation:
   BeefPercent = 60%
   ChickenPercent = 40%
   Total Cost of Ingredients per can = .52 cents per can
