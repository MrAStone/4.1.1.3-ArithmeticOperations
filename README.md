<pre lang=c#>
using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.InteropServices;
using System.Runtime.Remoting.Contexts;
using System.Text;
using System.Threading.Tasks;

namespace _4._1._1._3_ArithmeticOperations
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // addition
            //Add two integers
            int num1, num2;
            num1 = 12; num2 = 13;
            int num3 = num1 + num2;
            Console.WriteLine(num3);
            //add two decimals
            double dNum1, dNum2;
            dNum1 = 3.1596;
            dNum2 = 9.3642;
            double dNum3 = dNum1 + dNum2;
            Console.WriteLine(dNum3);
            // Add different numerical data types
            dNum3 = dNum3 + num3;
            Console.Write(dNum3);
            // num3 = dNum1 + num2; will error as result would be double not integer

            // subtraction
            // Subtract two integers
            num3 = num1 - num2;
            Console.WriteLine(num3);
            //subtract two decimals
            dNum3 = dNum1 - dNum3;
            Console.WriteLine(dNum3);
            //subtract different numerical data types
            dNum3 = num1 - dNum2;
            Console.WriteLine(dNum3);
            // num3 = dNum1 - num2;  will error as result would be double not integer

            // multiplication
            // integers
            num3 = num1 * num2;
            Console.WriteLine(num3);
            // decimals
            dNum3 = dNum1 * num2;
            Console.WriteLine(dNum3);
            // mixture
            dNum3 = num1 * dNum2;
            Console.WriteLine(dNum3);
            // num3 = dNum3 * num2;  will error as result would be double not integer

            // real division
            // Division in C# is based on the data type
            // To do real division the result must be stored in a decimal
            // The numbers used must also be stored in a decimal
            num1 = 7; num2 = 3;
            dNum3 = num1 / num2; // produces answer 2 as num1 and num2 are integers
            Console.WriteLine(dNum3);

            dNum1 = 7;
            dNum2 = 3;
            dNum3 = dNum1 / dNum2;
            Console.WriteLine(dNum3); // produces 2.333333.. which is correct decimal answer

            // If either number or divisor is decimal, a decimal will be produced

            dNum3 = dNum1 / num2;
            Console.WriteLine(dNum3);

            dNum3 = num1 / dNum2;
            Console.WriteLine(dNum3);

            // integer division, including remainders.
            // dividing two integers will produce integer division
            num1 = 9;
            num2 = 4;
            dNum3 = num1 / num2;
            Console.WriteLine(dNum3); // Produces 2 not 2.5
            Console.WriteLine(num1 / num2); // Also produces 2 as answer is integer
            //Finding remainder
            // Using MOD in c# uses the % symbol
            num3 = num1 % num2;
            Console.WriteLine(num3); // produces 1 as 9 / 4 has a remainder of 1 // 9 MOD 4 = 1

            // In C# the following is true
            // 11 / 2 = 5, 
            // 11 MOD 2 is written 11 % 2 = 1
            Console.WriteLine(11 / 2);
            Console.WriteLine(11 % 2);

            // exponentiation
            // use the Math class to do exponentiation
            Console.WriteLine(Math.Pow(2, 2));
            int result = Convert.ToInt32(Math.Pow(7, 2));// Math.Pow returns a Double 
            double dResult = Math.Pow(4, 9);
            // using variables
            int baseNum, exponent;
            baseNum = 12; // number
            exponent = 5; // power
            dResult = Math.Pow(baseNum, exponent);

            // rounding
            // use the Math class to do rounding
            Console.WriteLine(Math.Round(1.234, 2)); // rounds to 2 digits after decimal point
            double newResult = 3.0 / 7.0;
            Console.WriteLine(Math.Round(newResult, 3));
            Console.WriteLine(Math.Round(7.0 / 2.0)); // Output 4
            Console.WriteLine(Math.Round(-7.0 / 2.0)); // Ouput -4



            // truncation
            // use the Math class to do truncation
            Console.WriteLine(Math.Truncate(3.12314)); // Ouptut 3
            Console.WriteLine(Math.Truncate(-3.12314)); // Output -3
            Console.WriteLine(Math.Truncate(7.0 / 2.0)); // Output 3
            Console.WriteLine(Math.Truncate(-7.0 / 2.0)); // Ouput -3


        }
    }
}
