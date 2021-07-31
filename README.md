using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace caixa
{
    class Program
    {



        static void Main(string[] args)
        {
            Console.WriteLine("insria quantidas de notas disponiveis $100,00");
            int Quantidadenotas100 = int.Parse(Console.ReadLine());

            Console.WriteLine("insira quantidas de notas disponiveis $50,00");
            int Quantidadenotas50 = int.Parse(Console.ReadLine());

            Console.WriteLine("insira quantidas de notas disponiveis $20,00");
            int Quantidadenotas20 = int.Parse(Console.ReadLine());

            Console.WriteLine("insira quantidas de notas disponiveis $10,00");
            int Quantidadenotas10 = int.Parse(Console.ReadLine());

            /*
            int Quantidadenotas100 = 1;
            int Quantidadenotas50 = 3;
            int Quantidadenotas20 = 5;
            int Quantidadenotas10 = 100;
            int Quantidadenotas2 = 5;
            */
            bool caixa = true;
            while (caixa)
                {



              

                Console.WriteLine("insira o valor que deseja sacar");
                int valor = int.Parse(Console.ReadLine());
                // notas de 100
                int restante = valor / 100;
                int faltavl100 =  restante - Quantidadenotas100  ;

                if (faltavl100 < 0)
                {
                    faltavl100 = 0;
                }


                // Qauatitade ne notar e limites
                int quantidade100result = valor / 100;
                if (quantidade100result >= Quantidadenotas100)
                {
                    quantidade100result = Quantidadenotas100;
                }
                           
                int resto100 = valor % 100;

                //-notas de 50
                int restante50 = (resto100 + faltavl100 * 100) / 50;



                int faltavl50 = restante50 - Quantidadenotas50;

                if (faltavl50 < 0)
                {
                    faltavl50 = 0;
                }

                int resto50 = (resto100 + faltavl50 * 50) %50 ;
               

                int quantidade50result = (resto100 + faltavl100*100) / 50;

                if (quantidade50result >= Quantidadenotas50)
                {
                    quantidade50result = Quantidadenotas50;
                }


                //-notas ne 20
                int restante20 = (resto50 + faltavl50 * 50) / 20;
                int faltavl20 = restante - Quantidadenotas20;

                if (faltavl20 < 0)
                {
                    faltavl20 = 0;
                }
                

                int resto20 = (resto50 + faltavl50 * 50) %20 ;

                int quantidade20result = (resto50 + faltavl50 * 50) / 20;
                if (quantidade20result >= Quantidadenotas20)
                {
                    quantidade20result = Quantidadenotas20;
                }

                //notas de 10
                int restante10 = (resto50 + faltavl50 * 50) / 20;
                int faltavl10 = restante - Quantidadenotas10;

                if (faltavl20 < 0)
                {
                    faltavl20 = 0;
                }

               
                int resto10 = (resto20 + faltavl20 * 20) %10;
                int Sobra = faltavl10 + resto10;
                
                
                   
                
               
                int quantidade10result = (resto20 + faltavl20 * 20) / 10;
                if (quantidade10result >= Quantidadenotas10)
                {
                    quantidade10result = Quantidadenotas10;
                }

                if(Sobra<=0)
                {
                    Console.WriteLine("Quantidade de noats de $100,00 = " + quantidade100result);
                    Console.WriteLine("Quantidade de noats de $50,00 = " + quantidade50result);
                    Console.WriteLine("Quantidade de noats de $20,00 = " + quantidade20result);
                    Console.WriteLine("Quantidade de noats de $10,00 = " + quantidade10result);
                }
                else
                {
                    Console.WriteLine("Valor insufuciente ");
                }



                



                Console.WriteLine("--------------------------------" );
                

                Console.ReadLine();
                Console.Clear();

            }

            


        }
    }
}
