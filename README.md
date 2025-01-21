# Getter-setter-method
CODING:

import java.util.ArrayList;

import java.util.Scanner;

class Student {

// Fields

private int rollNumber;

private String name;

private double marks;

// Getter and Setter methods

public int getRollNumber() {

return rollNumber;

}

public void setRollNumber(int rollNumber) {

this.rollNumber = rollNumber;

}

public String getName() {

return name;

}

public void setName(String name) {

this.name = name;

}

public double getMarks() {

return marks;

}

public void setMarks(double marks) {

this.marks = marks;

}
// Method to display student details

public void displayDetails() {

System.out.println("Roll Number: " + rollNumber);

System.out.println("Name: " + name);

System.out.println("Marks: " + marks);

}

}

public class StudentDetails {

public static void main(String[] args) {

Scanner scanner = new Scanner(System.in);

ArrayList<Student> students = new ArrayList<>();

System.out.print("Enter the number of students: ");

int numberOfStudents = scanner.nextInt();

for (int i = 0; i < numberOfStudents; i++) {

System.out.println("\nEnter details for Student " + (i + 1) + ":");

Student student = new Student();

System.out.print("Enter Roll Number: ");

student.setRollNumber(scanner.nextInt());

scanner.nextLine(); // Consume newline

System.out.print("Enter Name: ");

student.setName(scanner.nextLine());

System.out.print("Enter Marks: ");

student.setMarks(scanner.nextDouble());
Add student to the list

students.add(student);

}

// Display all student details

System.out.println("\nStudent Details:");

for (int i = 0; i < students.size(); i++) {

System.out.println("\nStudent " + (i + 1) + ":");

students.get(i).displayDetails();

}

scanner.close();

}

}

OUTPUT:

Enter the number of students: 2

Enter details for Student 1:

Enter Roll Number: 101

Enter Name: John Doe

Enter Marks: 85.5

Enter details for Student 2:

Enter Roll Number: 102

Enter Name: Jane Smith

Enter Marks: 92.0

Student Details:

Student 1:

Roll Number: 101

Name: John Doe

Marks: 85.5
Student 2:

Roll Number: 102

Name: Jane Smith

Marks: 92.0 
