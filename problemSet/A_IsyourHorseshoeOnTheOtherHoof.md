
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
    