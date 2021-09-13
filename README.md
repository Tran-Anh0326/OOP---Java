

import java.util.Scanner;



public class anhtthe151377 {
/*    // bài 1 : Write a script that allows the user to enter a name and print say hello with this name
    public static void Name() {
        System.out.print("Nhap ten: ");
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        System.out.print("hello " + name);
        System.out.print("\n");
    }
    // bài 2 : Write a script that allows the user to enter scores and print out the rating results
    public static void Score() {
        System.out.print("Nhap diem: ");
        Scanner sc = new Scanner(System.in);
        double n = sc.nextDouble();
        if (n < 0 || n > 10) {
            System.out.print("Diem ban nhap khong hop le!");
        } else if (n >= 8) {
            System.out.print("Ban xep hang loai gioi ");
        } else if (n >= 7) {
            System.out.print("Ban xep hang loai kha ");
        } else if (n >= 4) {
            System.out.print("Ban xep hang loai trung binh ");
        } else
            System.out.print("Ban xep hang loai yeu ");

    }
    // bài 3: Write a script that allows the user to enter a number in the range 0-10, print out the number that has just been entered
    public static void Number() {
        Scanner sc = new Scanner(System.in);
        double n;
        do {
            System.out.print("\n");
            System.out.print("Nhap so trong khoang 0 - 10: ");
            n = sc.nextDouble();
        } while (n < 0 || n > 10);

        System.out.print("So ban vua nhap la: " + n);
    }
    // Bài 4: Write a script that allows the user to enter a number n in the range 1-5, which prints the result n! (use while, do while, for)
    public static void Factorial() {
        Scanner sc = new Scanner(System.in);
        int n, rs = 1;
        do {
            System.out.print("\n");
            System.out.print("Nhap so trong khoang 1 - 5: ");
            n = sc.nextInt();
        } while (n < 1 || n > 5);

        for (int i = 1; i <= n; i++) {
            rs *= i;
        }
        System.out.print("!n = " + rs);
    }
/*  //bài 5: Viết chương trình cho phép người dùng nhập và lưu mã số sinh viên vào file Student_info.txt trong thư mục data của project
    public static void fileWriter() {
        try {
            FileWriter w = new FileWriter("Student_info.txt");
            BufferedWriter buffer = new BufferedWriter(w);
            Scanner sc = new Scanner(System.in);
            System.out.print("Nhap ten: ");
            String name = sc.nextLine();
            String n = " ";
            System.out.print("Nhap ma sinh vien: ");
            String codeName = sc.nextLine();
            buffer.write(name);
            buffer.write(n);
            buffer.write(codeName);
            buffer.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
    //bài 6: Viết chương trình đọc và hiển thị thông tin sinh viên là tác giả của project (file trên)
    public static void fileReader() {
        try {
            FileReader r = new FileReader("Student_info.txt");
            BufferedReader bufferedReader = new BufferedReader(r);
            String line;

            while ((line = bufferedReader.readLine()) != null) {
                System.out.println(line);
            }
            r.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
*/    // bài 7 : Dựng menu với các chức năng sau, chọn và thực thi, hiển thị kết quả và hỏi chọn tiếp

    public static String a;
    public static int b;
    public static String c;

    public static String input() {

        Scanner sc = new Scanner(System.in);
        System.out.print("Name author: ");
        String name = sc.nextLine();
        a = name;
        return a;
    }
    public static int input1(){
        Scanner sc = new Scanner(System.in);
        System.out.print("Age: ");
        int age = sc.nextInt();
        b = age;
        return b;
    }
    public static String input2(){
        Scanner sc = new Scanner(System.in);
        System.out.print("Address: ");
        String address = sc.nextLine();
        c = address;
        return c;
    }



    public static void output() {


        System.out.println(a);
        System.out.println(b);
        System.out.println(c);


    }

    public static void printNumber() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap n de in tu 0 - n: ");

        int n;
                do{
                    n = sc.nextInt();
                }while(n<0);

        for (int i = 0; i <= n; i++) {
            System.out.print(i + " ");
        }
        System.out.print("\n");
    }

    public static void readNumber() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Chon so ban muon doc: ");
        int number = sc.nextInt();

        switch (number) {
            case 0:
                System.out.println(number + " = zero");
                break;
            case 1:
                System.out.println(number + " = one");
                break;
            case 2:
                System.out.println(number + " = two");
                break;
            case 3:
                System.out.println(number + " = three");
                break;
            case 4:
                System.out.println(number + " = four");
                break;
            case 5:
                System.out.println(number + " = five");
                break;
            case 6:
                System.out.println(number + " = six");
                break;
            case 7:
                System.out.println(number + " = seven");
                break;
            case 8:
                System.out.println(number + " = eight");
                break;
            case 9:
                System.out.println(number + " = nine");
                break;
            default:
                System.out.println("I don't know");
        }
    }

    public static void main(String[] args) {
/*        Name();
        Score();
        Number();
        Factorial();

        fileWriter();
        fileReader();

*/
        System.out.println("----------Menu------------");
        System.out.println("1: nhap thông tin tác giả\n" +
                "2: xem thông tin tác giả\n" +
                "3: thực hiện in chuỗi số 0-n\n" +
                "4: thực hiện đọc số từ 0-9\n" +
                "5: kết thúc chương trình");
        while (true) {
            System.out.print("Ban chon chuc nang so : ");
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            if (n < 1 || n > 5)
                System.out.println("Khong co chuc nang nay!");
            else {
                switch (n) {
                    case 1:
                        input();
                        input1();
                        input2();
                        break;
                    case 2:
                        output();
                        break;
                    case 3:
                        printNumber();
                        break;
                    case 4:
                        readNumber();
                        break;
                    case 5:
                        System.exit(0);
                }
            }

        }


    }
}
