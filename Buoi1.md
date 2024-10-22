**WELCOME TO JAVA**
# Document Buổi 1
**Hán Hữu Đăng**

## Mục lục
  
- [Document Buổi 1](#document-buổi-1)
  - [Mục lục](#mục-lục)
  - [Ngôn ngữ Java là gì?](#ngôn-ngữ-java-là-gì)
  - [Lý do ra đời của Java](#lý-do-ra-đời-của-java)
  - [Cách Java hoạt động](#cách-java-hoạt-động)
  - [Cấu trúc một chương trình Java](#cấu-trúc-một-chương-trình-java)
  - [Package là gì?](#package-là-gì)
  - [Syntax cơ bản](#syntax-cơ-bản)
    - [Khai báo biến nguyên thủy](#khai-báo-biến-nguyên-thủy)
    - [Vòng lặp](#vòng-lặp)
    - [Câu lệnh rẽ nhánh](#câu-lệnh-rẽ-nhánh)
    - [Mảng trong Java](#mảng-trong-java)
  - [Tổng quan về Class và Object](#tổng-quan-về-class-và-object)
    - [Từ khóa `this`](#từ-khóa-this)
    - [Constructor](#constructor)
    - [Access Modifier](#access-modifier)
    - [Getter và Setter](#getter-và-setter)
    - [Từ khóa `static`](#từ-khóa-static)

## Ngôn ngữ Java là gì?

Java là một ngôn ngữ lập trình hướng đối tượng (OOP), đa nền tảng, mạnh mẽ, an toàn và phổ biến.  Nó được thiết kế với mục tiêu "Write Once, Run Anywhere" (WORA), nghĩa là code Java được viết một lần có thể chạy trên nhiều nền tảng khác nhau mà không cần sửa đổi.

## Lý do ra đời của Java

* **Nhu cầu về ngôn ngữ lập trình độc lập nền tảng**: Vào thời điểm đó, hầu hết các ngôn ngữ lập trình đều phụ thuộc vào nền tảng, gây khó khăn cho việc phát triển phần mềm đa nền tảng.
* **Sự phát triển của lập trình hướng đối tượng**: OOP được xem là phương pháp lập trình hiện đại và hiệu quả, giúp giải quyết các vấn đề phức tạp trong phát triển phần mềm.
* **Mong muốn về một ngôn ngữ an toàn và mạnh mẽ**: Các ngôn ngữ lập trình hiện có lúc bấy giờ thường gặp các vấn đề về bảo mật và độ tin cậy.

## Cách Java hoạt động

Java hoạt động dựa trên nguyên lý "biên dịch một lần, chạy mọi nơi". Khi bạn viết code Java (.java), nó sẽ được biên dịch thành bytecode (.class). Bytecode là một dạng mã trung gian, không phụ thuộc vào nền tảng. 

Khi bạn chạy chương trình Java, máy ảo Java (JVM) sẽ đọc và thực thi bytecode. JVM có sẵn trên nhiều hệ điều hành khác nhau, cho phép code Java chạy trên bất kỳ nền tảng nào có cài đặt JVM.

Điều gì xảy ra khi chạy code Java (.java)?

1. **Biên dịch:** Code Java (.java) được biên dịch thành bytecode (.class) bởi trình biên dịch Java (javac).
2. **Nạp:** JVM nạp bytecode vào bộ nhớ.
3. **Xác minh:** JVM xác minh bytecode để đảm bảo tính an toàn và toàn vẹn.
4. **Thực thi:** JVM thực thi bytecode từng dòng một.

## Cấu trúc một chương trình Java

Một chương trình Java cơ bản thường có cấu trúc như sau:

```java
// Khai báo package (tùy chọn)
package com.example;

// Khai báo class
public class HelloWorld { 

  // Phương thức main - điểm bắt đầu của chương trình
  public static void main(String[] args) { 
    // Các câu lệnh trong chương trình
    System.out.println("Hello, world!"); 
  }
}
```

## Package là gì?

Package trong Java là một cơ chế để **tổ chức và quản lý các lớp** (class) và giao diện (interface). Nó giống như một hệ thống thư mục trong máy tính, giúp nhóm các lớp liên quan lại với nhau, tránh xung đột tên và làm cho code dễ đọc, dễ bảo trì hơn.

**Ví dụ:**

* `java.util`: Chứa các lớp tiện ích như `Scanner`, `ArrayList`, `HashMap`.
* `java.io`: Chứa các lớp làm việc với input/output như đọc/ghi file.
* `javax.swing`: Chứa các lớp để xây dựng giao diện đồ họa.

## Syntax cơ bản

### Khai báo biến nguyên thủy

Java có các kiểu dữ liệu nguyên thủy sau:

| Kiểu dữ liệu | Mô tả                                      | Phạm vi giá trị                       | Ví dụ              |
|--------------|-------------------------------------------|---------------------------------------|--------------------|
| `boolean`   | Lưu trữ giá trị đúng (`true`) hoặc sai (`false`) | `true` hoặc `false`               | `boolean isTrue = true;` |
| `byte`      | Số nguyên 8 bit có dấu                    | -128 đến 127                         | `byte age = 25;`    |
| `short`     | Số nguyên 16 bit có dấu                   | -32,768 đến 32,767                    | `short count = 1000;` |
| `int`       | Số nguyên 32 bit có dấu                   | -2,147,483,648 đến 2,147,483,647    | `int distance = 1000000;` |
| `long`      | Số nguyên 64 bit có dấu                   | -9,223,372,036,854,775,808 đến 9,223,372,036,854,775,807 | `long population = 7800000000L;` |
| `float`     | Số thực dấu chấm động 32 bit               | Khoảng ±3.40282347E+38F              | `float pi = 3.1415f;` |
| `double`    | Số thực dấu chấm động 64 bit               | Khoảng ±1.79769313486231570E+308     | `double balance = 1000.50;` |
| `char`      | Lưu trữ một ký tự Unicode                  | '\u0000' đến '\uffff' (0 đến 65,535) | `char initial = 'A';` |

```java
int age = 25;
double salary = 5000.50;
char grade = 'A';
boolean isEmployed = true;
```

### Vòng lặp

Vòng lặp được sử dụng để thực hiện một khối code nhiều lần. Java hỗ trợ các loại vòng lặp sau:

* **`for`:** Lặp với số lần xác định.

```java
for (int i = 0; i < 10; i++) {
  System.out.println(i);
}
```

* **`while`:** Lặp khi điều kiện còn đúng.

```java
int i = 0;
while (i < 10) {
  System.out.println(i);
  i++;
}
```

* **`do-while`:** Lặp ít nhất một lần, sau đó lặp khi điều kiện còn đúng.

```java
int i = 0;
do {
  System.out.println(i);
  i++;
} while (i < 10);
```

### Câu lệnh rẽ nhánh

Câu lệnh rẽ nhánh được sử dụng để thực hiện các khối code khác nhau dựa trên điều kiện. Java hỗ trợ các câu lệnh rẽ nhánh sau:

* **`if`:** Thực thi khối code nếu điều kiện đúng.

```java
if (age >= 18) {
  System.out.println("Bạn đã đủ tuổi trưởng thành.");
}
```

* **`if-else`:** Thực thi khối code `if` nếu điều kiện đúng, ngược lại thực thi khối code `else`.

```java
if (age >= 18) {
  System.out.println("Bạn đã đủ tuổi trưởng thành.");
} else {
  System.out.println("Bạn chưa đủ tuổi trưởng thành.");
}
```

* **`switch-case`:** Thực thi một trong nhiều khối code dựa trên giá trị của biểu thức.

```java
switch (grade) {
  case 'A':
    System.out.println("Xuất sắc");
    break;
  case 'B':
    System.out.println("Giỏi");
    break;
  default:
    System.out.println("Khá");
}
```

### Mảng trong Java

Mảng là một cấu trúc dữ liệu dùng để lưu trữ một tập hợp các phần tử có cùng kiểu dữ liệu.

**Khai báo mảng:**

```java
<kiểu_dữ_liệu>[] <tên_mảng>;
// Ví dụ:
int[] numbers;
```

**Khởi tạo mảng:**

```java
<tên_mảng> = new <kiểu_dữ_liệu>[kích_thước];
// Ví dụ:
numbers = new int[5]; // Mảng numbers có 5 phần tử kiểu int
```

**Khai báo và khởi tạo mảng cùng lúc:**

```java
<kiểu_dữ_liệu>[] <tên_mảng> = new <kiểu_dữ_liệu>[kích_thước];
// Ví dụ:
int[] numbers = new int[5];
```

**Khởi tạo mảng với giá trị ban đầu:**

```java
<kiểu_dữ_liệu>[] <tên_mảng> = {giá_trị_1, giá_trị_2, ...};
// Ví dụ:
int[] numbers = {1, 2, 3, 4, 5};
```

**Truy cập phần tử trong mảng:**

Sử dụng chỉ số (index) để truy cập phần tử trong mảng. Chỉ số bắt đầu từ 0.

```java
<tên_mảng>[chỉ_số]
// Ví dụ:
int firstNumber = numbers[0]; // Lấy phần tử đầu tiên (giá trị 1)
```

**Ví dụ về sử dụng mảng:**

```java
int[] ages = {25, 30, 22, 2, 8};
int sum = 0;
for (int i = 0; i < ages.length; i++) {
    sum += ages[i];
}
double averageAge = (double) sum / ages.length;
System.out.println("Tuổi trung bình: " + averageAge);
```

## Tổng quan về Class và Object

Lập trình hướng đối tượng (OOP) là một trong những nền tảng quan trọng của Java. OOP tập trung vào việc tổ chức code xung quanh các đối tượng, kết hợp dữ liệu và phương thức xử lý dữ liệu thành một đơn vị.

**Class:**

* Class là một **khuôn mẫu** (blueprint) để tạo ra các đối tượng.
* Class định nghĩa các **thuộc tính** (biến) và **hành vi** (phương thức) mà đối tượng sẽ có.
* Ví dụ: Class `Dog` có thể có các thuộc tính như `name`, `breed`, `age` và các phương thức như `bark()`, `eat()`, `sleep()`.

**Object:**

* Object là một **thể hiện cụ thể** của class.
* Mỗi object có các thuộc tính riêng biệt.
* Ví dụ:  `myDog` là một object của class `Dog` với `name = "Buddy"`, `breed = "Golden Retriever"`, `age = 3`.

**Ví dụ về Class và Object:**

```java
// Định nghĩa class Dog
public class Dog {
  // Thuộc tính
  String name;
  String breed;
  int age;

  // Phương thức
  public void bark() {
    System.out.println("Woof!");
  }

  public void eat(String food) {
    System.out.println("Chó đang ăn " + food);
  }
}

// Tạo object từ class Dog
public class Main {
  public static void main(String[] args) {
    Dog myDog = new Dog(); // Tạo object myDog
    myDog.name = "Buddy";
    myDog.breed = "Golden Retriever";
    myDog.age = 3;

    myDog.bark(); // Gọi phương thức bark() của object myDog
    myDog.eat("xương"); // Gọi phương thức eat() của object myDog
  }
}
```
### Từ khóa `this`

* `this` là một từ khóa tham chiếu đến **đối tượng hiện tại**.
* Sử dụng `this` để phân biệt giữa thuộc tính của đối tượng và biến cục bộ (local variable) có cùng tên.
* Ví dụ:

```java
public class Person {
  String name;

  public Person(String name) {
    this.name = name; // this.name là thuộc tính của object, name là tham số của constructor
  }
}
```

### Constructor

* Constructor là một **phương thức đặc biệt** được sử dụng để **khởi tạo đối tượng**.
* Constructor có **cùng tên với class** và **không có kiểu trả về**.
* Ví dụ:

```java
public class Person {
  String name;
  int age;

  // Constructor
  public Person(String name, int age) {
    this.name = name;
    this.age = age;
  }
}
```

### Access Modifier

Access modifier kiểm soát **khả năng truy cập** của các thành viên (thuộc tính và phương thức) trong class. 

| Access Modifier | Phạm vi truy cập                                           |
|-----------------|-----------------------------------------------------------|
| `public`       | Truy cập được từ mọi nơi.                                     |
| `private`      | Chỉ truy cập được trong class.                               |
| `protected`    | Truy cập được trong class, các lớp con và các lớp trong cùng package. |
| `(default)`    | Truy cập được trong cùng package.                            |

* Sử dụng access modifier để **bảo vệ dữ liệu** và **che giấu thông tin** không cần thiết.
* Ví dụ:

```java
public class Person {
  public String name; // Truy cập được từ mọi nơi
  private int age; // Chỉ truy cập được trong class Person
}
```

### Getter và Setter

* Getter và Setter là các phương thức được sử dụng để **lấy (get)** và **thiết lập (set)** giá trị cho các thuộc tính `private` của đối tượng.
* Sử dụng Getter và Setter để **kiểm soát việc truy cập và sửa đổi dữ liệu**, đảm bảo tính toàn vẹn của đối tượng.
* Ví dụ:

```java
public class Person {
  private int age;

  public int getAge() {
    return age;
  }

  public void setAge(int age) {
    if (age >= 0) {
      this.age = age;
    }
  }
}
```

### Từ khóa `static`

* `static` được sử dụng để khai báo các thành viên (thuộc tính và phương thức) **thuộc về class** chứ không phải đối tượng.
* Các thành viên static có thể được truy cập trực tiếp thông qua tên class mà không cần tạo đối tượng.
* Ví dụ:

```java
public class MathUtils {
  public static final double PI = 3.14159; // Thuộc tính static

  public static int sum(int a, int b) { // Phương thức static
    return a + b;
  }
}

// Sử dụng thành viên static
double circumference = 2 * MathUtils.PI * radius;
int total = MathUtils.sum(5, 3);
```


