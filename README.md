# COP-2334-1-Module-7-Programming-Assignment
This is a GitHub repository link for the Programming Assignment from Module 7.

// This program is used to calculate the total sales for five different types of salsa brands and flavors to display the highest selling and lowest selling salsa products.

// Include the necessary libraries
#include <iostream>
#include <string>
using namespace std; // Use the standard namespace

// Define the constants
int main() { // Start of the main function
  const int Brands = 5; // Number of brands
  const int Types = 5; // Number of types
  string salsa[Brands] = {"Tostitos Mild Salsa", "Cholula Medium", "Pace Sweet", "La Costena Hot", "Chi Chi's Zesty"}; // Array of salsa brands
  int jars[Types]; // Array of jars sold
  int total = 0; // Total jars sold
  int highestIndex = 0; // Index of highest selling salsa
  int lowestIndex = 0; // Index of lowest selling salsa
  for (int i = 0; i < Brands; i++) { // Start of the for loop
    cout << "Enter the number of jars sold for " << salsa[i] << ": "; // Prompt the user to enter the number of jars sold for each salsa brand
    cin >> jars[i]; // Read the number of jars sold for each salsa brand
    while (jars[i] < 0) { // Start of the while loop
      cout << "Please enter a positive number: "; // Prompt the user to enter a positive number
      cin >> jars[i]; // Read the number of jars sold for each salsa brand
    }
    total += jars[i]; // Add the number of jars sold for each salsa brand to the total
    if (jars[i] > jars[highestIndex]) { // Start of the if statement
      highestIndex = i; // Set the index of the highest selling salsa to the current index
    }
    if (jars[i] < jars[lowestIndex]) { // Start of the if statement
      lowestIndex = i; // Set the index of the lowest selling salsa to the current index
    } else { // Start of the else statement
      lowestIndex = i; // Set the index of the lowest selling salsa to the current index
    }
  }
  cout << "Sales Report" << endl; // Display the sales report
  for (int i = 0; i < Brands; i++) { // Start of the for loop
    cout << salsa[i] << ": " << jars[i] << " jars" << endl; // Display the number of jars sold for each salsa brand
  }
  cout << "Total sales: " << total << " jars" << endl; // Display the total number of jars sold
  cout << "Highest selling salsa brand and flavor: " << salsa[highestIndex] << endl; // Display the highest selling salsa brand and flavor
  cout << "Lowest selling brand and flavor: " << salsa[lowestIndex] << endl; // Display the lowest selling salsa brand and flavor
  return 0; // Return 0 to indicate successful program execution.
}
