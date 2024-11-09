# LAB-2-COMPLETE

**LAB TASK 1**

**1.Write a program that initializes Vector with 10 integers in it. Display all the integers and sum of these integer**


package com.mycompany.lab2labtask1;

public class Lab2labtask1 {

    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

    int sum = 0;
    for (int number : numbers) {
      sum += number;
    }

    System.out.println("Integers in the array:");
    for (int number : numbers) {
      System.out.println(number);
    }

    // Display the sum
    System.out.println("Sum of all integers: " + sum);
    }
}


**LAB TASK 2**

**2. Create a ArrayList of string. Write a menu driven program which:
      a. Displays all the elements
      b. Displays the largest String**


package com.mycompany.lab2labtask2;

import java.util.*;
public class Lab2labtask2 {

    public static void main(String[] args) {
         ArrayList<String> strings = new ArrayList<>(Arrays.asList("Aijaz", "Mobariz", "Wasay", "Talha" , "Hassam"));
        Scanner scanner = new Scanner(System.in);
        int choice;

        do {
            System.out.println("\n1. Display all elements");
            System.out.println("2. Display largest string");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");
            choice = scanner.nextInt();

            switch (choice) {
                case 1 -> System.out.println("Elements: " + strings);
                case 2 -> System.out.println("Largest String: " + Collections.max(strings, Comparator.comparingInt(String::length)));
                case 3 -> System.out.println("Exiting...");
                default -> System.out.println("Invalid choice! Try again.");
            }
        } while (choice != 3);

    }
}

**LAB TASK 3**

**3.	Create a Arraylist storing Employee details including Emp_id, Emp_Name, Emp_gender, Year_of_Joining (you can also add more attributes including these). Then sort the employees according to their joining year using Comparator and Comparable interfaces.**


package com.mycompany.lab2labtask3;

import java.util.*;

public class Lab2labtask3 {

    static class Employee implements Comparable<Employee> {
        int id;
        String name;
        String gender;
        int yearOfJoining;

        public Employee(int id, String name, String gender, int yearOfJoining) {
            this.id = id;
            this.name = name;
            this.gender = gender;
            this.yearOfJoining = yearOfJoining;
        }

        @Override
        public int compareTo(Employee other) {
            return Integer.compare(this.yearOfJoining, other.yearOfJoining);
        }

        @Override
        public String toString() {
            return "Employee{id=" + id + ", name='" + name + "', yearOfJoining=" + yearOfJoining + "}";
        }
    }

    public static void main(String[] args) {
        List<Employee> employees = Arrays.asList(
            new Employee(1, "Aijaz", "male", 2015),
            new Employee(2, "Sultan", "Male", 2013),
            new Employee(3, "Qamar", "Male", 2020)
        );

        Collections.sort(employees);
        System.out.println("Sorted Employees by Year of Joining:");
        employees.forEach(System.out::println);
    }
}

**LAB TASK 4**

**4. Write a program that initializes Vector with 10 integers in it.
         • Display all the integers 
         • Sum of the. 
         • Find Maximum Element in Vector.**


package com.mycompany.lab2labtask4;

import java.util.*;
public class Lab2labtask4 {

    public static void main(String[] args) {
        Vector<Integer> numbers = new Vector<>();
        numbers.add(5);
        numbers.add(12);
        numbers.add(7);
        numbers.add(19);
        numbers.add(3);
        numbers.add(25);
        numbers.add(10);
        numbers.add(8);
        numbers.add(15);
        numbers.add(6);

        System.out.println("Elements in the Vector: " + numbers);

        int sum = 0;
        for (int num : numbers) {
            sum += num;
        }
        System.out.println("Sum of elements: " + sum);

        int max = numbers.get(0);
        for (int num : numbers) {
            if (num > max) {
                max = num;
            }
        }
        System.out.println("Maximum element: " + max);
    }
}

**LAB TASK 5**

**5. Find the k-th smallest element in a sorted ArrayList**


package com.mycompany.lab2labtask5;
import java.util.*;

public class Lab2labtask5 {
    public static int findKthSmallest(List<Integer> list, int k) {
        Collections.sort(list);
        return list.get(k - 1);
    }

    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<>(Arrays.asList(5, 3, 8, 6, 2, 9));
        int k = 3;

        System.out.println("K-th smallest element: " + findKthSmallest(numbers, k));
    }
}

**LAB TASK 6**

**6. Write a program to merge two ArrayLists into one**


package com.mycompany.lab2labtask6;

import java.util.*;
public class Lab2labtask6 {

    public static void main(String[] args) {
        ArrayList<String> list1 = new ArrayList<>();
        list1.add("Aijaz");
        list1.add("Mobariz");
        list1.add("Wasay");

    
        ArrayList<String> list2 = new ArrayList<>();
        list2.add("Talha");
        list2.add("HAssam");
        list2.add("Khurram");


        ArrayList<String> mergedList = new ArrayList<>(list1);
        mergedList.addAll(list2);

        System.out.println("Merged ArrayList: " + mergedList);
    }
}

**HOME TASK 1**

**1. Create a Vector storing integer objects as an input. 
        a. Sort the vector
        b. Display largest number 
        c. Display smallest number**


package com.mycompany.lab2hometask1;
import java.util.*;
public class Lab2hometask1 {

    public static void main(String[] args) {
        Vector<Integer> numbers = new Vector<>(Arrays.asList(20, 3, 45, 1, 100));

        Collections.sort(numbers);
        System.out.println("Sorted Vector: " + numbers);

        System.out.println("Largest Number: " + Collections.max(numbers));
        System.out.println("Smallest Number: " + Collections.min(numbers));

    }
}

**HOME TASK 2**

**2.	Write a java program which takes user input and gives hashcode value of those inputs using hashCode () method.**


package com.mycompany.lab2hometask2;
import java.util.*;
public class Lab2hometask2 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter a string: ");
        String userInput = scanner.nextLine();
        
  
        int hashCode = userInput.hashCode();
        
        System.out.println("Hash code of the input string" + userInput + " is: " + hashCode);
    }
}

**HOME TASK 3**

**3.Scenario based 
Create a java project, suppose you work for a company that needs to manage a list of employees. Each employee has a unique combination of a name and an ID. Your goal is to ensure that you can track employees effectively and avoid duplicate entries in your system. 

Requirements
a.	Employee Class: You need to create an employee class that includes: 
• name: The employee's name (String)
• id: The employee's unique identifier (int). 
• Override the hashCode () and equals () methods to ensure that two employees are considered equal if they have the same name and id. 

b. Employee Management: You will use a HashSet to store employee records. This will help you avoid duplicate entries. 

c. Operations: Implement operations to:
 • Add new employees to the record. 
• Check if an employee already exists in the records. 
• Display all employees.**


package com.mycompany.lab2hometask3;

import java.util.*;

class Employee {
    String name;
    int id;

    public Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Employee employee = (Employee) obj;
        return id == employee.id && Objects.equals(name, employee.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, id);
    }

    @Override
    public String toString() {
        return "Employee{name='" + name + "', id=" + id + "}";
    }
}

public class Lab2hometask3 {

    public static void main(String[] args) {
        HashSet<Employee> employees = new HashSet<>();
        employees.add(new Employee("Aijaz", 1));
        employees.add(new Employee("Kon Talha", 2));

        System.out.println("Employees: " + employees);

    }
}

**HOME TASK 4**

**4.	Create a Color class that has red, green, and blue values. Two colors are considered equal if their RGB values are the same.**


package com.mycompany.lab2hometask4;

import java.util.*;

class Color {
    int red, green, blue;

    public Color(int red, int green, int blue) {
        this.red = red;
        this.green = green;
        this.blue = blue;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Color color = (Color) obj;
        return red == color.red && green == color.green && blue == color.blue;
    }

    @Override
    public int hashCode() {
        return Objects.hash(red, green, blue);
    }

    @Override
    public String toString() {
        return "Color{red=" + red + ", green=" + green + ", blue=" + blue + "}";
    }
}
public class Lab2hometask4 {

    public static void main(String[] args) {
        Color color1 = new Color(255, 0, 0);
        Color color2 = new Color(255, 0, 0);

        System.out.println("Colors are equal: " + color1.equals(color2));

    }
}
