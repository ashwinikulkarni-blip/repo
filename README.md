# repo
Find missing number in the sequence in c#- Learn how to find the missing number among the sequence of numbers from 1 to n with example Programs.  For Example following are the numbers from 1 to 6 as 1,2,3,5,6. The missing number in the above sequence is 4.  Input  1,2,3,5,6  Output  Missing Number : 4

...............................................................................................................................................
using System;
class Find_Missing_Number
    {
        static void Main(string[] args)
        {
            //array to find the missing number between 1 and 10
            // Simplicity, We will take number 1 to 10 i where Number 5 is missing in the sequence.
            int[] arr = { 1, 2, 3, 4, 6, 7, 8, 9, 10 };

            int missingNumber,Totalsum;
            // Accoreding to series rule, calculating sum of total numbers upto 10
            //sum of first n natutal numbers=n*(n+1)/2
            Totalsum = (arr.Length + 1) * (arr.Length + 2) / 2;

            // Missing number is calculating.
            foreach (int item in arr)
            {
                Totalsum = Totalsum - item;
            }
            missingNumber = Totalsum;

            Console.WriteLine("missing number  : {0}",missingNumber);
        }
    }

