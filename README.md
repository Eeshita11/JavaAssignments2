# package Package1;
import java.util.Scanner;

public class studentAttendance 
{
	public static void main(String[] args) 
	{
	Scanner scanner = new Scanner(System.in);
    String[] studentNames = new String[10];
    double[] attendancePercentages = new double[10];
    for (int i = 0; i < 10; i++) 
    {
        System.out.print("Enter the name of student " + (i + 1) + ": ");
        studentNames[i] = scanner.nextLine();
        System.out.print("Enter the attendance percentage for " + studentNames[i] + ": ");
        attendancePercentages[i] = scanner.nextDouble();
        scanner.nextLine();
    }
    System.out.println("Grades of the students:");

    for (int i = 0; i < 10; i++) 
    {
        String grade;
        switch ((int) attendancePercentages[i] / 10) 
        {
            //case 9:
            case 10:
                grade = "A";
                break;
            case 8:
                grade = "B";
                break;
            case 7:
                grade = "C";
                break;
            case 6:
                grade = "D";
                break;
            default:
                grade = "E";
        }
        System.out.println(studentNames[i] + ": " + grade);
    }
	}
}
   

