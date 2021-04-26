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
