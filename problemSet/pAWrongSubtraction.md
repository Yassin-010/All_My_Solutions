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
    
    