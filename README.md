//# BMI-calculator
//A c# (C-sharp) BMI calculator
using System;

namespace BMIcalculator
{
    class Bmi
    {
        static void Main(string[] args)
        {
            
            Console.WriteLine("Enter your age: ");
            int age = Convert.ToInt32(Console.ReadLine());
            
                while (age < 1) //using while loop as a conditional statement for the user prompt
                {
                   Console.WriteLine("There is no way you are that young :(");
                    //if the user enter an incorrect age the program will allow the user to correct that mistake 
                   Console.WriteLine("please enter your correct age: ");
                   age = Convert.ToInt32(Console.ReadLine());

                } while (age > 130)
                {
                   Console.WriteLine("There is no way you are that old :(");
                //if the user enter an incorrect age the program will allow the user to correct that mistake 
                Console.WriteLine("please enter your correct age: ");
                   age = Convert.ToInt32(Console.ReadLine());
                }

                //while loop for height
                Console.WriteLine("Enter your height in cm: ");
                double height = Convert.ToDouble(Console.ReadLine());
                while (height < 50)
                {
                   Console.WriteLine("height is too short to calculate :( ");
                    //the program allows the user to correct their Height
                   Console.WriteLine("Please enter the correct height");
                   height = Convert.ToDouble(Console.ReadLine());

                } while (height > 250)
                {
                   Console.WriteLine("height is too tall to calculate :( ");
                //the program allows the user to correct their Height
                   Console.WriteLine("Please enter the correct height");
                   height = Convert.ToDouble(Console.ReadLine());
                }

                //while loop for weight
                Console.WriteLine("Enter your weight in  kg: ");
                double weight = Convert.ToDouble(Console.ReadLine());
                while (weight < 30)
                {
                   Console.WriteLine("weight is too small to calculate :( ");
                //the program allows the user to correct their Weight
                   Console.WriteLine("Please enter the correct weight: ");
                   weight = Convert.ToDouble(Console.ReadLine());
                }
                while (weight > 2000)
                {
                   Console.WriteLine("weight is too big to calculate :( ");
                //the program allows the user to correct their Weight
                   Console.WriteLine("Please enter the correct weight: ");
                   weight = Convert.ToDouble(Console.ReadLine());
                }

                //calculating height in meters
                double mHeight = height / 100;

                //calculating BMI
                double bmi = weight / (mHeight * mHeight);
                Console.WriteLine("Your BMI is: " + bmi);
                // using the else...if statement for the possible out come for the BMI
                if (bmi < 47.1)
                {
                   Console.WriteLine("BMI is underweight \n" );
                }
                else if (bmi > 84.5)
                {
                   Console.WriteLine("BMI is Overwight \n");
                }
                else if (bmi > 100)
                {
                   Console.WriteLine("BMI is obese \n");
                }
                else if (bmi == 65.5)
                {
                   Console.WriteLine("BMI is great \n");
                }
                else
                {
                   Console.WriteLine("Incorrect bmi \n");
                }     
        }

    }    
}
