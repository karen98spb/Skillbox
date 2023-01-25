# Skillbox

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using static System.Net.Mime.MediaTypeNames;

namespace ConsoleApp_3._10
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //Console.Write("Задание 1. Приложение по определению чётного или нечётного числа\nВведите номер:");
            //int N = int.Parse(Console.ReadLine());
            //Console.WriteLine(N % 2 == 0 ? "Четное" : "Не четное");   // формула if, где then - это "?", else - это ":"
            //Console.WriteLine("Нажми Enter, чтобы продолжить");
            //Console.ReadLine();



            //Console.Write("Задание 2. Программа подсчёта суммы карт в игре «21»\nПривет! Сколько у Вас на руках карт?");
            //int R = int.Parse(Console.ReadLine());
            //string value;
            //double sum = 0;
            //for (int i = 1; i <= R; i++)                           // цикл, кот. испол. для прохождения через блок указанное число раз
            //{
            //    Console.Write($"Номинал {i} -й карты: ");
            //        value = Console.ReadLine();
            //    switch (value)                                     // удобно использовать вместо if, но не ifs
            //    {
            //        case "1": sum += 1; break;
            //        case "2": sum += 2; break;
            //        case "3": sum += 3; break;
            //        case "4": sum += 4; break;
            //        case "5": sum += 5; break;
            //        case "6": sum += 6; break;
            //        case "7": sum += 7; break;
            //        case "8": sum += 8; break;
            //        case "9": sum += 9; break;
            //        case "10":
            //        case "J":
            //        case "Q":
            //        case "K":
            //        case "T": sum += 10; break;                    // пустые условия заполняются вверх
            //        default:
            //            Console.WriteLine("Формат номинала не поддерживается");
            //            i--;                                                        // даем еще одну попытку
            //            break;
            //    }
            //}
            //Console.Write($"Сумма карт на руках: {sum}. ");
            //Console.WriteLine(sum > 22 ? "Вы проиграли..." : "Победа!");



            //Console.Write("Задание 3. Проверка простого числа:\n");
            //int P = int.Parse(Console.ReadLine());
            //int i1 = 2;
            //bool b = true;

            //while (i1 < P-1)                 // сколько раз выполнять цикл
            //{
            //    i1++;
            //    //Console.WriteLine(P % i1);
            //    if (P % i1 == 0)
            //            b = false;         // если в цикле выполнится условие равное 0,то b=false, если не найдется, то так и останется true, как по умолчанию.
            //}
            //if (b)
            //{
            //    Console.WriteLine("Простое число");
            //}
            //else
            //{
            //    Console.WriteLine("не является простым числом");
            //}




            //Console.Write("Задание 4. Наименьший элемент в последовательности:\n");
            //Console.WriteLine("Длина последовательности:");
            //int P2 = int.Parse(Console.ReadLine());
            //int min = int.MaxValue;
            //int i2 = 1;
            //do { 
            //    i2++;
            //    int Number = int.Parse(Console.ReadLine());
            //    if (Number < min)
            //    {
            //        min = Number;
            //    }

            //} while (i2 <= P2);
            //Console.WriteLine($"int.MinValue = {min}");


            Console.Write("Задание 5. Игра «Угадай число»\n");
            Console.Write("Максимальное целое число диапазона:");
            int P3 = int.Parse(Console.ReadLine());
            Random randomize = new Random();
            int randomIntResult = randomize.Next(P3);
            string value;
            while (true)
            {
                value = Console.ReadLine();
                if (value == string.Empty)
                {
                    Console.WriteLine($"Устал? Окей, randomIntResult = {randomIntResult}");
                    Console.ReadKey();
                    break;
                }
                else
                {
                    int value5 = int.Parse(value);
                    if (randomIntResult > value5)
                    {
                        Console.WriteLine("Ваше число меньше загаданного...");
                    }
                    else if (randomIntResult < value5)
                    {
                        Console.WriteLine("Ваше число больше загаданного...");
                    }
                    else
                    {
                        Console.WriteLine("Красава");
                        Console.ReadKey();
                        break;
                    }
                }
            }
           
            
        }
    }
}
