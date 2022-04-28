
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
    