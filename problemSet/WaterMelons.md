
    //start WaterMelons
    import java.io.BufferedReader;
    import java.io.BufferedWriter;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.io.OutputStreamWriter;
    import sun.nio.cs.StreamEncoder;
    
    public class Prcticeing_1 {

    public static void main(String[] args) throws IOException {
        //A4-Watermelion
        BufferedReader reader =new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter writer =new BufferedWriter(new OutputStreamWriter(System.out));
        int num=Integer.parseInt(reader.readLine());
        if(num>=1 && num<=100)
            if(num%2==0 && num!=2)
                writer.write("yes");
            else writer.write("no");
        writer.newLine();
        writer.flush();
    }

    }
    
    //end WaterMelons