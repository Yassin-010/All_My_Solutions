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
    