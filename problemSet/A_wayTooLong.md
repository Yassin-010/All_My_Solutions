
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
    
