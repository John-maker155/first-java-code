import java.util.Scanner;
public class calculator{
    public static void main(String[] args){
      Scanner sc = new Scanner(System.in);
        int choice;
        double firstnum;
        double secondnum;
        double result;
        boolean enable;

       System.out.print("Enable Calculator (true/false) => ");
       enable = sc.nextBoolean();

        if(enable == true){
      do {
        System.out.println("==> CALCULATOR <==");
        System.out.println("1.Addition");
        System.out.println("2.Subtraction");
        System.out.println("3.Multiplication");
        System.out.println("4.Division");
        System.out.println("5.Exit");
        System.out.print("Enter your Selected Option:");
        choice = sc.nextInt();

      switch (choice){
      case 1:
      System.out.print("Enter First num: ");
      firstnum = sc.nextDouble();
      System.out.print("Enter Second num: ");
      secondnum = sc.nextDouble();
      result = firstnum + secondnum;
      System.out.println("Result:" + result);
      break;
      case 2:
      System.out.print("Enter First num: ");
      firstnum = sc.nextDouble();
      System.out.print("Enter Second num: ");
      secondnum = sc.nextDouble();
      result = firstnum - secondnum;
      System.out.println("Result:" + result);
      break;
      case 3:
      System.out.print("Enter First num: ");
      firstnum = sc.nextDouble();
      System.out.print("Enter Second num: ");
      secondnum = sc.nextDouble();
      result = firstnum * secondnum;
      System.out.println("Result:" + result);
      break;
      case 4:
      System.out.print("Enter First num: ");
      firstnum = sc.nextDouble();
      System.out.print("Enter Second num: ");
      secondnum = sc.nextDouble();

      if(firstnum <= 0){
            System.out.println("Sorry cannot procceed, Please try again");
          }else if(secondnum <= 0){
            System.out.println("Sorry cannot procceed, Please try again");
          }else{
            result = firstnum / secondnum;
            System.out.println("Result: " + result);
          }
      break;
      case 5:
      System.out.println("Thank you for using Calculator!!");
      break;
      default:
      System.out.println("Invalid Input, Please Try Again");
        }
      }while (choice != 5);
    }
    else{
      System.out.println("enable == [false]");
    }
    sc.close();
  }
}

