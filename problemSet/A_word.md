    //start A_word
    // solution number 1
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;

    public class P2__A_Word {

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        String text = reader.readLine();
        int count = 0;
        for (int i = 0; i < text.length(); i++) {

            char ch = text.charAt(i);
            if (ch >= 65 && ch <= 90) {
                count++;

            }

        }

        if (count > text.length() - count ) {
            writer.write(text.toUpperCase());
        } else {
            writer.write(text.toLowerCase());
        }

        writer.flush();
    }
    }
    //end solution number 1
    
    //start solution tow
    
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    
    public class Main {

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer = new BufferedWriter(new OutputStreamWriter(System.out));

        String text = reader.readLine();
        int count = 0, space = 0;
        for (int i = 0; i < text.length(); i++) {

            char ch = text.charAt(i);
            if (ch >= 65 && ch <= 90) {
                count++;

            }
            if (text.charAt(i) == ' ') {
                space++;
            }
        }

        if (count > text.length() - count - space) {
            writer.write(text.toUpperCase());
        } else {
            writer.write(text.toLowerCase());
        }

        writer.flush();
    }
    }
    
    //end solution tow
    //end A_word
    