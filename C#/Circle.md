using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Crircle
{
    class Program
    {
        static void Main(string[] args)
        {
            // Various Variables used within the main method
            double radius, Area, Circum; 
            string input;

            //User enters the radius
            Console.WriteLine("Please enter radius: ");//could also use Write instead of WriteLine
            input = Console.ReadLine(); // Accept input as string
            radius = Convert.ToDouble(input); // Convert input to double

            Calculate cal = new Calculate();// Creating an object Area from Class Calculate 
           Calculate adder = new Calculate(); //Creating an object circumfereence from Class Calculate

            Area = cal.CirArea(radius); // variable Area accepts the result from the class Calculate
            Circum = adder.Circumference(radius);

            Console.WriteLine("The Area of the circle is " + Area); //("The  circumference of the circle is " + Circum);// Print the Result
            Console.WriteLine("The Circumference of the circle is " + Circum);
            Console.ReadKey();
        }
    }
    class Calculate
    {
        public double CirArea(double rad)
        {
            double Area;// Variable decleration

            Area = 3.142 * rad * rad ;// Calculation of the Area

            return Area; // Value of Area is returned to Main method
        }

        public double Circumference(double rad)
        {
            double Cir;// Variable decleration

            Cir = 2 * 3.142 * rad;// Calculation of the Circumference

            return Cir; // Valu of Circumference is returned to Main method
        }
    }


}
