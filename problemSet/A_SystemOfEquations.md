
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
    
    