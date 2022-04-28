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
    