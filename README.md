# black-Jack
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace BlackJack
    {
        class Program
        {
            static Random lop = new Random();
            static int points;
            static int Randomnumber()
            {

                int intd = lop.Next(0, 13);
                return intd;
            }
            static void checkpoints(int c1, int d1)
            {

                if (c1 + d1 <= 15)
                {
                    Console.WriteLine("its a Draw take another card from dealer");
                }
                else if (c1 + d1 >= 22)
                {
                    Console.WriteLine("You loose re bet");
                }
                else
                {
                    Console.WriteLine("You won");
                }
                Console.WriteLine(c1+d1);
                Console.ReadLine();
            }

            static void Main(string[] args)
            {
                int c, d;
                for (int i = 0; i <= 5; i++)
                {

                    c = Randomnumber();
                    d = Randomnumber();


                    Console.WriteLine(c);
                    Console.WriteLine(d);
                
                    checkpoints(c, d);

                }


            }

        }
    }

  
