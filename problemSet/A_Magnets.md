
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
    