
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
    