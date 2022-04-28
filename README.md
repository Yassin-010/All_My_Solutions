# All_My_Solutions


    //start A_word
    // solution number 1
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    public class P2__A_Word {

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        String text = reader.readLine();
        int count = 0;
        for (int i = 0; i < text.length(); i++) {

            char ch = text.charAt(i);
            if (ch >= 65 && ch <= 90) {
                count++;

            }

        }

        if (count > text.length() - count ) {
            writer.write(text.toUpperCase());
        } else {
            writer.write(text.toLowerCase());
        }

        writer.flush();
    }
    }
    //end solution number 1
    
    //start solution tow
    
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    public class Main {

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        String text = reader.readLine();
        int count = 0, space = 0;
        for (int i = 0; i < text.length(); i++) {

            char ch = text.charAt(i);
            if (ch >= 65 && ch <= 90) {
                count++;

            }
            if (text.charAt(i) == ' ') {
                space++;
            }
        }

        if (count > text.length() - count - space) {
            writer.write(text.toUpperCase());
        } else {
            writer.write(text.toLowerCase());
        }

        writer.flush();
    }
    }
    
    //end solution tow
    //end A_word
    
    
    
    
    //start A_wordCorection
    //start first solution
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    public class P3_word_correction {

    public static boolean vowels(char c) {

        return ((c == 'a') || (c == 'e') || (c == 'u') || (c == 'i') || (c == 'y') || (c == 'o'));

    }

    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));
        int n = Integer.parseInt(reader.readLine());

        String word = reader.readLine();
        int count = 0;

        for (int i = 0; i < word.length(); i++) {
            if (vowels(word.charAt(i))) {
                count++;//4
                if (count <= 1) {
                    writer.write("" + word.charAt(i));
                }

            } else {
                count = 0;
                writer.write("" + word.charAt(i));
            }

        }

        writer.newLine();
        writer.flush();

    }
    }
    //end first solution
    
    
    //start second solution
    
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    public class p2 {


    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));
        int n = Integer.parseInt(reader.readLine());

        boolean[] vowels = new boolean[26];
        vowels['a' - 'a'] = true;
        vowels['e' - 'a'] = true;
        vowels['i' - 'a'] = true;
        vowels['y' - 'a'] = true;
        vowels['o' - 'a'] = true;
        vowels['u' - 'a'] = true;

        String word = reader.readLine();
        boolean v = false;
        for (int i = 0; i < word.length(); i++) {
            char c = word.charAt(i);

            if (vowels[c - 'a']) {

                if (!v) {
                    writer.write("" + c);
                }
                v = true;

            } else {
                v = false;
                writer.write("" + c);
            }

        }

        writer.newLine();
        writer.flush();

    }
    }
    //end second solution
    //end A_wordCorection
    
    
    
    
    
    //start  A_SystemOfEquations
    
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    import java.util.StringTokenizer;
    
    public class PA_SystemOfEquations {

    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        StringTokenizer ns = new StringTokenizer(reader.readLine());

        int n = Integer.parseInt(ns.nextToken());
        int m = Integer.parseInt(ns.nextToken());
        int counter = 0;

        if (1 <= n && m <= 1000) {

            for (int a = 0; a <= m; a++) {
                for (int b = 0; b <= n; b++) {

                    int num1 = (int) Math.pow(a, 2);
                    int result1 = num1 + b;

                    if (result1 == n) {

                        int num2 = (int) Math.pow(b, 2);
                        int result2 = num2 + a;

                        if (result2 == m) {
                            counter++;
                        }
                    }
                }

            }

            System.out.println(counter);

        } else {
            System.out.println("Invalid input");
        }

        writer.flush();
    }

    }
    
    //end A_SystemOfEquations
    
    
    
    
    
    
    
    
    
    
    
    
    //start A_wayTooLong
    import java.io.BufferedInputStream;
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;

        import javax.swing.plaf.synth.SynthOptionPaneUI;

    public class P3_word_correction {

    public static void cheack(String str) {
        System.out.print(str.charAt(0));
        System.out.print(str.length() - 2);
        System.out.println(str.charAt(str.length() - 1));
    }

    public static void main(String[] args) throws IOException {
        // A4-Watermelion
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));
        int num = Integer.parseInt(reader.readLine());

        // String text = reader.readLine();
        String arr[] = new String[num];
        int i = 0;
        for (i = 0; i <= num - 1; i++) {
            arr[i] = reader.readLine();

        }

        for (i = 0; i < arr.length; i++) {
            if (arr[i].length() <= 10) {
                // writer.write(arr[i]);
                System.out.println(arr[i]);

            } else
                cheack(arr[i]);
        }

        writer.flush();

    }

    }
    //end A_wayTooLong
    





    
    //start WaterMelons
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    import sun.nio.cs.StreamEncoder;
    
    public class Prcticeing_1 {

    public static void main(String[] args) throws IOException {
        //A4-Watermelion
        BufferedReader reader =new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer =new BufferedWriter(new OutputStreamWriter(System.out));
        int num=Integer.parseInt(reader.readLine());
        if(num>=1 && num<=100)
            if(num%2==0 && num!=2)
                writer.write("yes");
            else writer.write("no");
        writer.newLine();
        writer.flush();
    }

    }
    
    //end WaterMelons
    
    //stat A_IsyourHorseshoeOnTheOtherHoof
    import java.io.*;
    import java.util.Scanner;
    import java.util.StringTokenizer;
    
    public class A_IsYourHorseshoeOnTheOtherHoof {
    static BufferedReader reader;
    static BufferedWriter writer;
    static StringTokenizer token;
    static long num;
    static int arr[];
    static int counter = 0;
    public static int getResult() throws IOException {
    reader = new BufferedReader(new InputStreamReader(System.in));
    writer = new BufferedWriter(new OutputStreamWriter(System.out));
    token = new StringTokenizer(reader.readLine());
    arr = new int[4];
    arr[0] = (int) Long.parseLong(token.nextToken());
    arr[1] = (int) Long.parseLong(token.nextToken());
    arr[2] = (int) Long.parseLong(token.nextToken());
    arr[3] = (int) Long.parseLong(token.nextToken());
    int i = 1;
    for (int j = 0; j < 3; ) {

            for (; i < 4; i++)
                if (arr[j] == arr[i])
                    counter++;
            j++;
            i = j + 1;
        }
        if (counter % 2 == 0 && counter > 5) counter = counter / 2;
        else if (counter % 2 != 0 && counter > 1) counter--;
        return counter;
    }
    public static void main(String[] args) throws IOException {
        getResult();
        writer.write("" + counter);
        writer.newLine();
        writer.flush();

    }
    }
    
    //end A_IsyourHorseshoeOnTheOtherHoof
    



    
    //stat A_Magnets
    import java.io.*;
    
    public class A_Magnets {

    static int numberOfLines;
    static int input;
    static int inputFirstOne;
    static int counter = 1;
    static BufferedReader reader;
    static BufferedWriter writer;
    static int array[];

    public static int returnRuslt(int ifo) throws IOException {
        inputFirstOne = ifo;//10
        array = new int[numberOfLines];//[numberOfLines]
        for (int i = 1; i < numberOfLines; i++) { // with out ecual
            input = Integer.parseInt(reader.readLine());
            array[0] = inputFirstOne;//10
            array[i] = input;//10

            if (array[i] == array[i - 1]){

            } else counter++;


        }
        return counter;
    }

    public static void main(String[] args) throws IOException {

        reader = new BufferedReader(new InputStreamReader(System.in));
        writer = new BufferedWriter(new OutputStreamWriter(System.out));

        numberOfLines = Integer.parseInt(reader.readLine());
        inputFirstOne = Integer.parseInt(reader.readLine());
        returnRuslt(inputFirstOne);

        writer.write("" + counter);
        writer.flush();
    }
    
    }
    
    //end A_Magnets
    
    
    
    
    
    
    // Start A_StonesOnTheTable
    
    import java.io.*;
    public class A_StonesOnTheTable {
    static int count;
    static String text;
    static int num;
    public static int returnResult(int n,String t,int c){
    num=n;
    text=t;
    count=c;

        for (int i = 1; i < num; i++) {
            if(text.charAt(i) == 'R' && text.charAt(i - 1) == 'R')
                count ++;

            else if(text.charAt(i) == 'B' && text.charAt(i - 1) == 'B')
                count ++;

            else if(text.charAt(i) == 'G' && text.charAt(i - 1) == 'G')
                count ++;

        }
        return count;

    }

    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));


        num=Integer.parseInt(reader.readLine());
        text=reader.readLine();

        returnResult(num,text,count);

        writer.write(""+count);
        writer.newLine();
        writer.flush();

    }
    }
    
    //end A_StonesOnTheTable
    
    
    
    
    // Start  P_A_BeotifulMarix
    import java.util.Scanner;
    
    
    public class P_A_BeotifulMarix {

    public static void main(String[] args)  {
        // First solution
        Scanner in=new Scanner(System.in);
        int arr[][]=new int [5][5];
        int r=0,c=0,counter=0;

        for(int i=0;i<5;i++){
            for (int j = 0; j < 5; j++) {
                arr[i][j]=in.nextInt();
                if (arr[i][j]==1) {
                    counter+=Math.abs(i-2)+Math.abs(j-2);
                }
            }
        }
        System.out.println(counter);

    }
    }
    
    //second solution
    /*
    Scanner in=new Scanner(System.in);
    int arr[][]=new int [5][5];
    int r=0,c=0,counter=0;

    for(int i=0;i<5;i++){
      for (int j = 0; j < 5; j++) {
      arr[i][j]=in.nextInt();
          if (arr[i][j]==1) {
              r=i;c=j;
          }
      }
    }

         if (r==c&&(r==0||r==4))
             counter=4;
         else if(r==c&&(r==1||r==3))
             counter=2;
         else if(r==0&&c==1 || r==1&&c==0 || r==3&&c==4 ||r==4&&c==3)
             counter=3;
         else
    counter=Math.abs(r-c);

    System.out.println(counter);

    }
    }
    */
    
    
    // End  P_A_BeotifulMarix
    //end P_A_BeotifulMatrix
    
    
    
    
    
    //start PA_TrickySum
    // Start  PA_TrickySum
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    
    public class PA_TrickySum {

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));
        int t = Integer.parseInt(reader.readLine());
        long sum = 0, valu = 0, result = 0;

        for (int p = 0; p < t; p++) {
            long n1 = Long.parseLong(reader.readLine());

            sum = n1 * (n1 + 1) / 2;
            for (long i = 1; i < n1 + 1; i = (long) i * 2) { // prooooooooofessional !!!!
                valu += i;
            }
            result = sum - (valu * 2);
            writer.write("" + result);
            writer.newLine();
            valu = 0;

        }
        writer.newLine();
        writer.flush();

    }

    }
    
    
    // End  PA_TrickySum
    //end PA_TrickySum
    
    
    
    
    //start A_BeautifulYear
    import java.io.*;
    
    public class A_BeautifulYear {

    static String numOfYear;
    static int num;

    public static int returnResult(String y) {
        numOfYear = y;
        num = Integer.parseInt((numOfYear));
        num++;
        numOfYear = String.valueOf(num);
        for (int i = 0; i < 3;) {

            if (numOfYear.charAt(0) == numOfYear.charAt(i + 1)) {
                num++;
                numOfYear = String.valueOf(num);
                i = 0;

            }
            else if (numOfYear.charAt(1) == numOfYear.charAt(2) || numOfYear.charAt(1) == numOfYear.charAt(3)) {
                num++;
                numOfYear = String.valueOf(num);
                i = 0;

            } else if (numOfYear.charAt(2) == numOfYear.charAt(3)) {
                num++;
                numOfYear = String.valueOf(num);
                i = 0;

            } else if (i == 2) break;
            else i++;
        }
        return num;
    }
    public static void main(String[] args) throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        returnResult(reader.readLine());
        writer.write("" + num);
        writer.flush();


    }
    }
    
    //end A_BeautifulYear
    
    
    
    
    //start P_C_AlternatingSubsequence
    import java.io.*;
    import java.util.StringTokenizer;
    
    public class P_C_AlternatingSubsequence {
    static BufferedReader reader;
    static BufferedWriter writer;
    static StringTokenizer token;
    static int numberOfLines;
    static int bigArray[];
    static int smallArray[];
    static int numberOfElementsInBigArray;
    static int maximum;
    static long sum = 0;
    public static int Buffers() throws IOException {

        reader = new BufferedReader(new InputStreamReader(System.in));
        writer = new BufferedWriter(new OutputStreamWriter(System.out));

        numberOfLines = Integer.parseInt(reader.readLine());

        return numberOfLines;
    }
    public static int maxmumInSmallArray(int[] t) {
        maximum = t[0];
        for (int i = 1; i < t.length; i++) {
            if (t[i] > maximum) {
                maximum = t[i];
            }
        }
        return maximum;
    }
    public static long getResult() throws IOException {

        numberOfElementsInBigArray = Integer.parseInt(reader.readLine());
        bigArray = new int[numberOfElementsInBigArray];
        token = new StringTokenizer(reader.readLine());
        bigArray[0] = Integer.parseInt(token.nextToken());

        for (int i = 0, j = 0; i < numberOfElementsInBigArray; ) { //10 peroids
            if (i < numberOfElementsInBigArray - 1)
                bigArray[i + 1] = Integer.parseInt(token.nextToken());

            // 1----------------------------------------------------
            if ((i == bigArray.length - 1) && ((bigArray[j] > 0 && bigArray[i] > 0) || (bigArray[j] < 0 && bigArray[i] < 0))) {
                smallArray = new int[(i - j) + 1];
                for (int k = 0; k < (i - j) + 1; k++) {
                    smallArray[k] = bigArray[j + k];
                }
                sum += maxmumInSmallArray(smallArray);
                j = i;
                break;
            }
            // 2 ------------------------------------------------
            if (bigArray[i] > 0 && bigArray[j] > 0) {
                i++;
                continue;
            } else if (bigArray[i] < 0 && bigArray[j] < 0) {
                i++;
                continue;
            } else {
                smallArray = new int[i - j];
                for (int k = 0; k < (i - j); k++) {
                    smallArray[k] = bigArray[j + k];
                }
                sum += maxmumInSmallArray(smallArray);
                j = i;
                i++;
            }
            // 3----------------------------------------------------
            i--;
            if ((i == bigArray.length - 1) && (((bigArray[bigArray.length - 1] < 0) && (bigArray[bigArray.length - 2] > 0)) || ((bigArray[bigArray.length - 1] > 0) && (bigArray[bigArray.length - 2] < 0)))) {
                sum += bigArray[bigArray.length - 1];
                break;
            }
            i++;
        }
        return sum;
    }
    public static void main(String[] args) throws IOException {
        Buffers();
        for (int i = 0; i < numberOfLines; i++) {
            getResult();
            writer.write("" + sum);
            sum = 0;
            writer.newLine();
        }
        writer.flush();
    }
    }
    //end P_C_AlternatingSubsequence
    
    
    
    //start pAWrongSubtraction
    import java.io.*;
    import java.util.StringTokenizer;
    
    public class pAWrongSubtraction {

    //static Long tokNum1=0L;
    static Long tokNum1;
    static int tokNum2;


    public static Long returnResult(Long t1, int t2) {
        tokNum1 = t1;
        tokNum2 = t2;
        for (int i = 0; i < tokNum2; i++) {
            if (tokNum1 % 10 == 0) {
                tokNum1 = tokNum1 / 10;
            } else {
                tokNum1--;
            }
        }
        return tokNum1;
    }


    public static void main(String[] args) throws IOException {


        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        StringTokenizer tokenizer = new StringTokenizer(reader.readLine());
        tokNum1 = Long.parseLong(tokenizer.nextToken());//1000000000
        tokNum2 = Integer.parseInt(tokenizer.nextToken());//9

        returnResult(tokNum1, tokNum2);

        writer.write(tokNum1 + "");


        writer.newLine();
        writer.flush();
    }
    
    }
    //end pAWrongSubtraction
    
    
    









