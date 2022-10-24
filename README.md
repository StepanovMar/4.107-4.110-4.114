using System;
class Programm
{
    static void Main(string[] args)
    {
        while (true)
        {
         int n;
         bool k;
         while (true)
         {
             try
             {
                 Console.Write("Номер месяца, принимает значение от 1 до 12:");
                 n = Convert.ToInt16(Console.ReadLine());
                 if (n >= 1 & n <= 12)
                 {
                     Console.Write("Если год невисокосный, Введите 0:");
                     k = Convert.ToBoolean(Console.Read());
                     break;
                 }
                 else
                     Console.WriteLine("Вход не поддерживается, повторите ввод");
             }
             catch (FormatException)
             {
                 Console.WriteLine("Это не число");
             }
         }
         switch (n)
         {
             case 2:
                 if (k == true)
                     Console.WriteLine("В этом месяце 28 дней");
                 else
                     Console.WriteLine("В этом месяце 29 дней");
                 break;
         }
         switch (n)
         {
             case 4:
                 Console.WriteLine("В этом месяце 30 дней");
                 break;
             case 6:
                 Console.WriteLine("В этом месяце 30 дней");
                 break;
             case 9:
                 Console.WriteLine("В этом месяце 30 дней");
                 break;
             case 11:
                 Console.WriteLine("В этом месяце 30 дней");
                 break;
             default:
                 Console.WriteLine("В этом месяце 31 дней");
                 break;
         }
         Console.WriteLine("Нажмите любую клавишу чтобы продолжить или ESC для выхода");
         ConsoleKey e = Console.ReadKey().Key;
         if (e == ConsoleKey.Escape)
             break;
         Console.WriteLine("Клавиша {0}", e);
     }
 }
}
