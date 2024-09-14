# Program-CPP_TLS24

#include <iostream>
#include <cmath> // Include cmath for sqrt function

int main() {
  double side1, side2, side3; 

  // Get input from the user
  std::cout << "Enter the length of side 1: ";
  std::cin >> side1;
  std::cout << "Enter the length of side 2: ";
  std::cin >> side2;
  std::cout << "Enter the length of side 3: ";
  std::cin >> side3;

  // Check if the sides form a valid triangle (Triangle Inequality)
  if (side1 + side2 > side3 && side1 + side3 > side2 && side2 + side3 > side1) {

    // Calculate the area using Heron's formula
    double s = (side1 + side2 + side3) / 2; // Semi-perimeter
    double area = sqrt(s * (s - side1) * (s - side2) * (s - side3));

    std::cout << "The area of the triangle is: " << area << std::endl;

  } else {
    std::cout << "Invalid triangle! The sum of any two sides must be greater than the third side.\n"; 
  }

  return 0;
}
