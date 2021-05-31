# ggmC-
```
﻿using System;
using System.Collections.Generic;

using static System.Console;

namespace ConsoleApp1
{
    class Program
    {

        class MyMath
        {
            public static double PI = 3.141592;
        }
        class Product
        {
            public string name;
            public int price;
        }
        class Product
        {
            public string name = "default";
            public int price = 1000;
        }
        class Car
        {
            public int carNumber;
        }
        class Student
        {
            public string name;
            public int grade;
        }
        static void Main(string[] args)
        {
        List<Car> list = new List<Car>();

        Car c1 = new Car(); c1.carNumber = 100; list.Add(c1);
        Car c2 = new Car(); c2.carNumber = 200; list.Add(c2);
        Car c3 = new Car(); c3.carNumber = 300; list.Add(c3);
        Car c4 = new Car(); c4.carNumber = 400; list.Add(c4);
        Car c5 = new Car(); c5.carNumber = 500; list.Add(c5);
        foreach (Car item in list)
        {
            WriteLine(item.carNumber);
        }

        ClassA ca = new ClassA();

        Product productA = new Product() { name = "감자", price = 2000 };
        Product productB = new Product() { name = "고구마", price = 3000 };

        List<Product> li = new List<Product>();

        li.Add(new Product() { name = "p1", price = 1000 });
        li.Add(new Product() { name = "p2", price = 2000 });
        li.Add(new Product() { name = "p3", price = 3000 });

        foreach (Product item in li)
        {
            WriteLine(item.name + ":" + item.price);
        }


        MyMath m = new MyMath();
        WriteLine(MyMath.PI);

        List<Student> list = new List<Student>();
        list.Add(new Student() { name = "김성규", grade = 4 });
        foreach (Student item in list)
        {
            WriteLine(item.name + ":" + item.grade);
        }
        }

        //연습문제
        //1번 
        // O
        // X
        // O
        // X
        // O
        // O
        // O
        // X

        //2번
        //List, list
        //Car, car
        //Product,product
        //Dictionary, dictionary

        //3번
        //3

        //4번
        //4

        //5번
        //class Unit
        //{
        //    public string name;
        //    public int mineral;
        //    public int supply;
        //    public int hp;
        //    public int attack;
        //}
        // Unit scv = new Unit() {name = "건설로봇", mineral = 50,supply = 1,life = 45,damage = 5};

        //6번
        //class Book
        //{
        //    public string name;
        //    public DateTime Date;
        //    public string auther;
        //    public string ower;
        //    public string publish;
        //    public string seniorEdit;
        //    public string producer;
        //    public string edit;
        //    public string design;
        //}
        //Book b = new Unit() {name = "PHP 프로그래밍 입문",Date = "2013년 5월 20일",auther = "황재호",ower = "김태헌",publish = "한빛아카데미(주",seniorEdit = "김현용",producer = "김이화",edit = "김이화",design = "여동일"};

        //7번
        //    class Pet
        //    {
        //        public string name;
        //        public int age;
        //    }
        //    class Person
        //    {
        //        public string name;
        //        public string add;
        //        public List<Pet> pet;
        //    }
        //    Pet cloud = new Pet() { name = "구름", age = 7 };
        //    Pet star = new Pet() { name = "별", age = 1 };
        //    Person person = new Person() { name = "윤인성", add = "서울특별시 강서구", pet = new List<Pet>() { cloud, star } };
        //    Pet wind = new Pet() { name = "바람", age = 4 };
        //    person.pet.Add(wind);
    }
}
```
## 
```
﻿using System;
using System.Collections;
using System.Threading;


using static System.Console; // using class

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            //int a = 30;
            //string result = a == 30 ? "참" : "거짓"; 
            //WriteLine(result);

            //string result = (10 % 2) == 0 ? "짝수" : "홀수";
            //WriteLine(result);


            //ArrayList a = null;
            //a = new ArrayList();

            //a?.Add("야구");   // == if(a != null) a.Add("야구");
            //a?.Add("축구");
            //WriteLine($"Count : {a?.Count}");
            //WriteLine($"{a?[0]}");
            //WriteLine($"{a?[1]}");


            //int a = 1;
            //WriteLine("a      : {0:D5} (0x{0:X8})", a);
            //WriteLine("a << 1 : {0:D5} (0x{0:X8})", a << 1);
            //WriteLine("a << 2 : {0:D5} (0x{0:X8})", a << 2);
            //WriteLine("a << 3 : {0:D5} (0x{0:X8})", a << 5);

            //int b = 255;
            //WriteLine("b      : {0:D5} (0x{0:X8})", b);
            //WriteLine("b >> 1 : {0:D5} (0x{0:X8})", b >> 1);
            //WriteLine("b >> 2 : {0:D5} (0x{0:X8})", b >> 2);
            //WriteLine("b >> 3 : {0:D5} (0x{0:X8})", b >> 5);


            //int? b = null;
            //WriteLine($"{b ?? 10}");

            //string str2 = null;
            //WriteLine($"{str2 ?? "0"}");

            //string str = null;
            //if (str == null)
            //    Write("0");
            //else
            //    Write($"{str}");

            //int a = -5;
            //if (a < 0)
            //    WriteLine("음수");
            //else if (a == 0)
            //    WriteLine("0");
            //else
            //    WriteLine("양수");

            //int a = int.Parse(ReadLine());
            //if (a % 2 == 0)
            //    WriteLine("짝수");
            //else
            //    WriteLine("홀수");

            //int number = int.Parse(ReadLine());
            //if (number > 0 && number % 2 == 0)
            //    WriteLine("0보다 큰 짝수");
            //else if (number > 0)
            //    WriteLine("0보다 큰 홀수");
            //else
            //    WriteLine("0보다 작거나 같은 수.");

            //switch (조건식)
            //{
            //    case 상수1:
            //        break;
            //    case 상수2:
            //        break;
            //    case 상수3:
            //        break;
            //    default: // 생략 가능
            //        break;
            //}

            //object obj = null;
            //string s = ReadLine();
            //if (int.TryParse(s, out int out_i))
            //    obj = out_i;
            //else if (float.TryParse(s, out float out_f))
            //    obj = out_f;
            //else
            //    obj = s;

            //switch(obj)
            //{
            //    case int i:
            //        WriteLine($"{i}는 int 형식입니다.");
            //        break;
            //    case float f:
            //        WriteLine($"{f}는 float 형식입니다.");
            //        break;
            //    default:
            //        WriteLine($"{obj}는 모르는 형식입니다.");
            //        break;
            //}
```
### 
```
using System;
using System.Collections;
using System.Threading;

using static System.Console;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            //long start = DateTime.Now.Ticks;
            //long count = 0;

            //while (start + (10000000) > DateTime.Now.Ticks)
            //{
            //    count++;
            //}
            //Console.WriteLine(count + "만큼 반복했습니다");

            //int[] Array = { 1, 2, 3, 4, 5, 6 };

            //for (int i = Array.Length - 1; i >= 0; i--)
            //{
            //        Write(Array[i] + " ");
            //}

            //for(int i = 0; i < Array.length; i++)
            //{
            //        WriteLine(Array[i] + " ");
            //}

            //foreach (int i in Array)
            //{
            //        WriteLine(i);
            //}

            //string[] array = { "사과", "배", "포도", "딸기", "바나나" };

            //foreach (string item in array)
            //{
            //    WriteLine(item);
            //}

            //char[] i = { '0', '1', '2', '3', '4', '5', '6', '7', '8', '9' };

            //foreach (char a in i)
            //{
            //    WriteLine(a);
            //}


            //int count = 10;
            //for (int i = 0; i < count; i++)
            //{
            //    for (int j = 0; j < i + 1; j++)
            //    {
            //        Write('*');
            //    }
            //    WriteLine();
            //}

            //for (int i = 0; i < count; i++)
            //{
            //    for (int j = 0; j < count - i; j++)
            //    {
            //        Write(' ');
            //    }
            //    for (int j = 0; j < i + 1; j++)
            //    {
            //        Write('*');
            //    }
            //    WriteLine();
            //}

            //for (int i = 0; i < count; i++)
            //{
            //    for (int j = (count - 1) - i; j >= 0; j--)
            //    {
            //        Write(' ');
            //    }
            //    for (int j = 0; j < i + 1; j++)
            //    {
            //        Write('*');
            //    }
            //    for (int j = 0; j < i; j++)
            //    {
            //        Write('*');
            //    }
            //    WriteLine();
            //}

            //for (int i = 0; i < count; i++)
            //{
            //    for (int j = 0; j < count - i; j++)
            //    {
            //        Write(' ');
            //    }
            //    for (int j = 0; j < 2 * i + 1; j++)
            //    {
            //        Write('*');
            //    }
            //    WriteLine();
            //}

            //for (int i = 0; i < count; i++)
            //{
            //    for (int j = count - 1; j >= 0; j--)
            //    {
            //        for (int k = 0; k < count - i; k++)
            //        {
            //            Write(' ');
            //        }
            //        Write('*');
            //    }
            //    WriteLine();
            //}

            //while(true)
            //{
            //    Write("숫자를 입력해주세요(짝수 입력시 종료) : ");
            //    int input = int.Parse(ReadLine());

            //    if( input % 2 == 0)
            //    {
            //        break;
            //    }
            //}

            //for (int i = 0; i < 100; i++)                               //goto 쓰지마셈
            //{
            //    for (int j = 0; j < 100; j++)
            //    {
            //        if (i == 50 && j == 50)
            //        {
            //            goto Label;
            //        }
            //    }
            //Label:
            //}

            //for(int i = 0; i < 100; i++)
            //{
            //    if (i % 2 == 0)
            //    {
            //        continue;
            //    }
            //    WriteLine(i);
            //}

            //string input = "감자 고구마 토마토";
            //string[] inputs = input.Split(new char[] { ' ' });

            //foreach (string item in inputs)
            //{
            //    WriteLine(item);
            //}

            //string input = " test   \n";
            //WriteLine("::" + input.Trim() + "::");
            //Read();

            //string[] array = {"감자", "고구마", "토마토", "가지"};
            //WriteLine(string.Join(",", array));

            //WriteLine("첫 번째 출력");
            //Thread.Sleep(1000);
            //WriteLine("두 번째 출력");
            //Thread.Sleep(1000);
            //WriteLine("세 번째 출력");

            //int x = 1;
            //while (x < 50)
            //{
            //    Clear();
            //    SetCursorPosition(x, 5);

            //    if (x % 3 == 0)
            //    {
            //        WriteLine("@__");
            //    }
            //    else if (x % 3 == 1)
            //    {
            //        WriteLine("@_-");
            //    }
            //    else
            //    {
            //        WriteLine("@-_");
            //    }

            //    Thread.Sleep(100);
            //    x++;
            //}

            //while(true)
            //{
            //    ConsoleKeyInfo info = ReadKey();
            //    switch(info.Key)
            //    {
            //        case ConsoleKey.UpArrow:
            //            WriteLine("위로 이동");
            //            break;
            //        case ConsoleKey.RightArrow:
            //            WriteLine("우로 이동");
            //            break;
            //        case ConsoleKey.DownArrow:
            //            WriteLine("아래로 이동");
            //            break;
            //        case ConsoleKey.LeftArrow:
            //            WriteLine("좌로 이동");
            //            break;
            //        default:
            //            return;
            //    }
            //}
```
###### level up
```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

using static System.Console;

namespace ConsoleApp2
{
    class Player
    {
        private float level;
        private float exp;

        private void LevelUp()
        {
            float a = 0;

            level = 1f;
            if(exp != 0)
            {
                a = exp;
                for (int i = 0; i < a; i++)
                {
                    level++;
                    WriteLine("레벨업 :" + (level - 1) + "->" + level);
                }
            }
        }
        public void AddExp(float ex)
        {
            exp = 0;
            exp += ex / 100;
            LevelUp();
            WriteLine("현재 레벨 : " + level + " 경헙치 : ");
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Player p = new Player();
            p.AddExp(210);

        }
    }
}

```
