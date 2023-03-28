using NUnit.Framework;
using Калькулятор;

namespace TestProject1
{
    public class Tests
    {
        [SetUp]
        public void Setup()
        {
        }

        [Test]
        public void Testsum()
        {
            float a = 4;
            float b = 10;
            float expected = 14;
            float actual = Class1.Sum(a, b);
            Assert.AreEqual(expected, actual);
        }

        [Test]
        public void TestMinus()
        {
            float a = 4;
            float b = 10;
            float expected = -6;
            float actual = Class1.Minus(a, b);
            Assert.AreEqual(expected, actual);
        }
        [Test]
        public void TestUmn()
        {
            float a = 4;
            float b = 10;
            float expected = 40;
            float actual = Class1.Umn(a, b);
            Assert.AreEqual(expected, actual);
        }
        [Test]
        public void TestDel()
        {
            float a = 4;
            float b = 10;
            float expected = 0.4f;
            float actual = Class1.Del(a, b);
            Assert.AreEqual(expected, actual);
        }
        [Test]
        public void TestDel0()
        {
            float a = 4;
            float b = 0;
            float expected = 0f;
            float actual = Class1.Del(a, b);
            Assert.AreEqual(expected, actual);
        }
    }
}



----------------------------------------------------------------------------------------------------

using System;

namespace Калькулятор
{
     publiuc class Class1
    {
       public static float Sum(float a, float b)
        {
            return a + b;
        }
        public static float Minus(float a, float b)
        {
            return a - b;
        }
        public static float Umn(float a, float b)
        {
            return a * b;
        }
        public static float Del(float a, float b)
        {
            float del = 0;
                if (b == 0)
            {
                Console.WriteLine("Error");
            }
            else del = a / b;
            return del;
        }


    }

}
