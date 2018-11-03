# Quadractic-Solver-Linear-Intersention
This program will ask the user for the a,b, and c of a quadratic and will return the vertex, y int, as well as the zeros. Additionally, it will ask the user for a linear function's m and b and it will return the points at which the parabola and the line will intersect.


#written by Natasha


print("Hello fellow user. Input a quadratic and I will solve for the zeros, y intercept, and the vertex.")

a = float(input("What would you like the a value to be?"))
b = float(input("What would you like the b value to be?"))
c = float(input ("What would you like the c value to be?"))
#Process the user input

import math

if b == 0:
  print("The vertex is (0, 0).")
else:
  x_value_vertex_ = float(-b/2 * a)

  y_value_vertex_ = ((a * (x_value_vertex_**2)) + (b * x_value_vertex_) + c)
  print("The vertex is (" + str(x_value_vertex_) + ", " + str(y_value_vertex_) + ").")

if c == 0:
  print("The y intercept is (0, 0).")
else:
  print("The y intercept is (0, " + str(c) + ").")

discriminant_ = (b**2 - 4*a*c)

if discriminant_ < 0:
  print("There are no x intercepts in this porabola.")
  
elif discriminant_ == 0:
  answer_1 = float(-b / (2 * a))
  if answer_1 == 0:
    print("There is one x intercept. It is (0, 0).")
  else:
    print("There is one x intercept. It is (" + str(answer_1) + ", 0).")

else:
  answer_1 = float(-b + math.sqrt(b**2 - 4*a*c)) / (2 * a)
  answer_2 = float(-b - math.sqrt(b**2 - 4*a*c)) / (2 * a)
  print("Your quadratic has two x intercepts. They are (" + str(answer_1) + ", 0) and (" + str(answer_2) + ", 0).")

print("Give me a linear function to see if it intersects this porabola.")

m = float(input("Give me the slope of your line (m)."))
b_2 = float(input("Give me the y intercept of your line (b)."))
  

new_b = (b - m)
new_c = (c - b_2)
  
discriminant_2 = (new_b**2 - 4*a*new_c)

if discriminant_2 < 0:
  print("These functions do not intersect.")
  
elif discriminant_2 == 0:
  intersection_1_x = float(-new_b / (2 * a))
  intersection_1_y = float(m*intersection_1_x) + b_2
  
  print("There is one point of intersection. It is (" + str(intersection_1_x) + ", " + str(intersection_1_y) + ").")
    
else:
  intersection_2_x = float(-new_b + math.sqrt(new_b**2 - 4*a*new_c)) / (2 * a)
  intersection_2_y = (m*intersection_2_x) + b_2
  intersection_3_x = float(-new_b - math.sqrt(new_b**2 - 4*a*new_c)) / (2 * a)
  intersection_3_y = (m*intersection_3_x) + b_2
  print("Your quadratic and linear functions have two points of intersection. They are (" + str(intersection_2_x) + ", " + str(intersection_2_y) + ") and (" + str(intersection_3_x) + ", " + str(intersection_3_y) + ").")
  
  
  
  
  
  
  
