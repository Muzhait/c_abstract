# Первый урок по курсу C#


##  Команды языка программирования C#

* dotnet new console - создание проекта

* dotnet run - запуск программы/приложения

* Write(); - вывод в одну строку

* WriteLine(); - в конце переход на новую строку

* ReadLine(); - считать строку из терминала

* string - тип данных строка

* int - тип данных целое число

* double  - тип данных вещественное число

* bool - логический тип данных правда или ложь (true и false)

* new Random().Next(min, max) - даст случаное целое число от min до max - 1

* .ToLower() - для перевода в нижний регистр как бы не ввел пользователь текст

* Console.Clear(); - очистка консоли

* Console.SetCursorPosirion(10. 4); - указание отступа, от левого и верхнего края, кол-во символов




## Примеры кода языка программирования C#

<!--- Вывод привет мир -->
### Привет мир
* Console.WriteLine("Hello, World!");

<!--- приветствие пользовотеля -->
### Привет пользователь
* Console.WriteLine("Введите Ваше имя сударь "); <!--- просим ввести имя -->
*  string username = Console.ReadLine(); <!--- ввод имени, где string обозночения что будет текст, строка, username  переменная которая будет хранить имя, Console.ReadLine консоль для ввода имени -->
* Console.WriteLine("Приветики, ");
* Console.WriteLine(username);
* При данном вводе Приветик и имя пользователя будет выводится на разных строках

### Привет пользователь с выводом в одну строку
* Console.Write("Введите Ваше имя сударь ");
* string username = Console.ReadLine();
* Console.Write("Приветики, ");
* Console.Write(username);

### Сумма заданых чисел
* int numberA = 3;
* int numberB = 4;
* Console.WriteLine(numberA + numberB);

### Сумма заданых чисел с присвоеннием суммы как переменная
* int numberA = 317;
* int numberB = 483;
* int result = numberA + numberB;
* Console.WriteLine(result);

### Сумма с генератором случайных чисел 
* int numberA = new Random().Next(15,47);
* Console.WriteLine(numberA);
* int numberB = new Random().Next(1,15);
* Console.WriteLine(numberB);
* int result = numberA + numberB;
* Console.WriteLine(result);

### Деление
<!--- double заменене на int, вместо целых чисел чтоб при делении указывался остаток -->
* double numberA = 120;
* double numberB = 80;
* Console.WriteLine(numberA / numberB);


### Особой приветствие какого то пользователя
<!--- ToLower переделаывай регистр на нижний имя введенное пользователем, что сокращает ошибку при сравнении имени -->
* Console.Write("Введите свое имя о драгоценнейщий пользователь: ");
* string username = Console.ReadLine();
* 
* if(username.ToLower() == "карим")
* {
*     Console.WriteLine("Добро пожаловать о великий Карим, достойнейщий из достойных, свет и надежда нашего государства!");
* }
* else
* {
*     Console.Write("Ну заходи раз пришел, ");
*     Console.WriteLine(username);
* }

### Поиск макс числа с заданными параметрами
* int a = 1;
* int b = 2;
* int c = 6;
* int d = 8;
* int e = 4;
* 
* int max = a;
* 
* if (a > max) max = a;
* if (b > max) max = b;
* if (c > max) max = c;
* if (d > max) max = d;
* if (e > max) max = e;
* 
* Console.Write("Максимальное число = ");
* Console.WriteLine(max);


### Отрисовка точек в середине отрезка
Console.Clear();

int xa = 40, ya = 1, 
    xb = 1, yb = 30,
    xc = 80, yc = 30;

Console.SetCursorPosition(xa, ya);
Console.WriteLine("+");

Console.SetCursorPosition(xb, yb);
Console.WriteLine("*");

Console.SetCursorPosition(xc, yc);
Console.WriteLine("#");

int x = xa, y = xb;

int count = 0;

while (count < 10000)
* {
  *  int what = new Random().Next(0, 3);
   * if (what == 0)
    * {
      *  x = (x + xa) / 2;
       * y = (y + ya) / 2;
   * }

*    if (what == 1)
 *   {
  *      x = (x + xb) / 2;
   *     y = (y + yb) / 2;
   * }
   * if (what == 2)
   * {
    *    x = (x + xc) / 2;
     *   y = (y + yc) / 2;
*     }

   * Console.SetCursorPosition(x, y);
   * Console.WriteLine("@");
   * count = count + 1; //count++ сокращени
* }



## Полезности и советы

* https://github.com/iksergey/gitignore/blob/main/VisualStudio.gitignore - список для гитигнор
