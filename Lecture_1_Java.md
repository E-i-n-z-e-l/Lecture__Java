**Настройка рабочего места**

**Шаг 1:**
Java JDK https://www.oracle.com/java/technologies/downloads/

**Шаг 2:**
Extension Pack VS Code
https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-javapack

**Шаг 3:**
Установить расширения на Java в VS code

**При желаниии:**
https://www.jetbrains.com/ru-ru/idea/
println(“Hello world”);


**Структура простой программы**

/**

Program

*/

public class Program {

 public static void main(String[] args) {

 System.out.println("Goodbye world");

 
 }

}



**Комментирование**

/* - начало комментария и можно писать все что угодно
*/ - конец комментария
// - обычный комментарий


**Типы данных**

boolean - true and false
int - целочисленный
short - это знаковый 16-битовый тип. Его диапазон — от -32768 до 32767.
float - хранит число с плавающей точкой от -3.4*1038 до 3.4*1038 и занимает 4 байта
double - хранит число с плавающей точкой от ±4.9*10-324 до ±1.7976931348623157*10308 и занимает 8 байт
char - хранит одиночный символ в кодировке UTF-16 и занимает 2 байта, поэтому диапазон хранимых значений от 0 до 65535
byte - хранит целое число от -128 до 127 и занимает 1 байт
long - хранит целое число от –9 223 372 036 854 775 808 до 9 223 372 036 854 775 807 и занимает 8 байт


**Массивы**

**Одномерные**

public class Program {
	public static void main(String[] args) {
		int[] arr = new int[10];
		System.out.println(arr.length); // 10
		arr = new int[] { 1, 2, 3, 4, 5 };
	System.out.println(arr.length); // 5
	}
}


**Многомерные**

public class Program {
	public static void main(String[] args) {
		int[] arr[] = new int[3][5];
		for (int[] line : arr) {
			for (int item : line) {
				System.out.printf("%d ", item);
			}
			System.out.println();
		}
	}
}




**Многомерные**

public class Program {
	public static void main(String[] args) {
		int[][] arr = new int[3][5];

		for (int i = 0; i < arr.length; i++) {
			for (int j = 0; j < arr[i].length; j++) {
				System.out.printf("%d ", arr[i][j]);
			}
			System.out.println();
		}
	}
}


**Преобразования**

public class Program {
 public static void main(String[] args) {
 int i = 123; double d = i;
 System.out.println(i); // 123
 System.out.println(d); // 123.0
 d = 3.1415; i = (int)d;
 System.out.println(d); // 3.1415
 System.out.println(i); // 3
 d = 3.9415; i = (int)d;
 System.out.println(d); // 3.9415
 System.out.println(i); // 3
 byte b = Byte.parseByte("123");
 System.out.println(b); // 123
 b = Byte.parseByte("1234");
 System.out.println(b); // NumberFormatException: Value out of range
 }
}

**Получение данных из терминала**

**Строки**

import java.util.Scanner;
public class Program {
	public static void main(String[] args) {
		Scanner iScanner = new Scanner(System.in);
		System.out.printf("name: ");
		String name = iScanner.nextLine();
		System.out.printf("Привет, %s!", name);
		iScanner.close();
	}
}


**Некоторые примитивы**

import java.util.Scanner;
public class Program {
	public static void main(String[] args) {
		Scanner iScanner = new Scanner(System.in);
		System.out.printf("int a: ");
		int x = iScanner.nextInt();
		System.out.printf("double a: ");
		double y = iScanner.nextDouble();
		System.out.printf("%d + %f = %f", x, y, x + y);
		iScanner.close();
}}


**Проверка на соответствие получаемого типа**

import java.util.Scanner;
public class Program {
	public static void main(String[] args) {
		Scanner iScanner = new Scanner(System.in);
		System.out.printf("int a: ");
		boolean flag = iScanner.hasNextInt();
		System.out.println(flag);
		int i = iScanner.nextInt();
		System.out.println(i);
		iScanner.close();
 	} }


**Форматированный вывод**

public class Program {
 public static void main(String[] args) {
 int a = 1, b = 2;
 int c = a + b;
 String res = a + " + " + b + " = " + c;
 System.out.println(res);
 }
}


**Виды спецификаторов**


%d: целочисленных значений
%x: для вывода шестнадцатеричных чисел
%f: для вывода чисел с плавающей точкой
%e: для вывода чисел в экспоненциальной форме,
например, 3.1415e+01
%c: для вывода одиночного символа
%s: для вывода строковых значений

public class Program {
 public static void main(String[] args) {

 float pi = 3.1415f;
 System.out.printf("%f\n", pi); // 3,141500
 System.out.printf("%.2f\n", pi); // 3,14
 System.out.printf("%.3f\n", pi); // 3,141
 System.out.printf("%e\n", pi); // 3,141500e+00
 System.out.printf("%.2e\n", pi); // 3,14e+00
 System.out.printf("%.3e\n", pi); // 3,141e+00
 }
}

**Функции и методы**

public class Program {
 static void sayHi() {
 System.out.println("hi!");
 }
 static int sum(int a, int b) {
 return a+b;
 }
 static double factor(int n) {
 if(n==1)return 1;
 return n * factor(n-1);
 }
 public static void main(String[] args) {
 sayHi(); // hi!
 System.out.println(sum(1, 3)); // 4
 System.out.println(factor(5)); // 120.0
 }}


**Циклы**

**Цикл while**

public class Program {
 public static void main(String[] args) {
 int value = 321;
 int count = 0;
 while (value != 0) {
 value /= 10;
 count++;
 }
 System.out.println(count);
 }

**Цикл do while**

public class Program {
 public static void main(String[] args) {
 int value = 321;
 int count = 0;
 do {
 value /= 10;
 count++;
 } while (value != 0);
 System.out.println(count);
 }
}



**Операторы для управления циклами — continue и break.**

Выполнение следующей итерации цикла — continue.
Прерывание текущей итерации цикла — break.
* ближайшего к оператору
}


**Оператор цикла for**
public class Program {
 public static void main(String[] args) {
 int s = 0;
 for (int i = 1; i <= 10; i++) {
 s += i;
 }
 System.out.println(s);
 }
}


**Работа с файлами**

**оздание и запись\ дозапись**

import java.io.FileWriter;
import java.io.IOException;
public class Program {
 public static void main(String[] args) {
 try (FileWriter fw = new FileWriter("file.txt", false)) {
 fw.write("line 1");
 fw.append('\n');
 fw.append('2');
 fw.append('\n');
 fw.write("line 3");
 fw.flush();
 } catch (IOException ex) {
 System.out.println(ex.getMessage());
 }
 } }

**Чтение, Вариант посимвольно**

import java.io.*;
public class Program {
 public static void main(String[] args) throws Exception {
 FileReader fr = new FileReader("file.txt");
 int c;
 while ((c = fr.read()) != -1) {
 char ch = (char) c;
 if (ch == '\n') {
 System.out.print(ch);
 } else {
 System.out.print(ch);
 }
 }
 } }

**Вариант построчно**

import java.io.*;
public class Program {
 public static void main(String[] args) throws Exception {
 BufferedReader br = new BufferedReader(new FileReader("file.txt"));
 String str;
 while ((str = br.readLine()) != null) {
 System.out.printf("== %s ==\n", str);
 }
 br.close();
 }
}

**Задачи для самоконтроля**
1. Задана натуральная степень k. Сформировать случайным
образом список коэффициентов (значения от 0 до 100)
многочлена многочлен степени k.
*Пример: k=2 => 2*x? + 4*x + 5 = 0 или x? + 5 = 0 или 10*x? = 0
2. Даны два файла, в каждом из которых находится запись
многочлена. Сформировать файл содержащий сумму
многочленов.