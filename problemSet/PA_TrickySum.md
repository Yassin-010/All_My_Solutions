
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
    
    