
    // Start  P_A_BeotifulMarix
    import java.util.Scanner;
    
    
    public class P_A_BeotifulMarix {

    public static void main(String[] args)  {
        // First solution
        Scanner in=new Scanner(System.in);
        int arr[][]=new int [5][5];
        int r=0,c=0,counter=0;

        for(int i=0;i<5;i++){
            for (int j = 0; j < 5; j++) {
                arr[i][j]=in.nextInt();
                if (arr[i][j]==1) {
                    counter+=Math.abs(i-2)+Math.abs(j-2);
                }
            }
        }
        System.out.println(counter);

    }
    }
    
    //second solution
    /*
    Scanner in=new Scanner(System.in);
    int arr[][]=new int [5][5];
    int r=0,c=0,counter=0;

    for(int i=0;i<5;i++){
      for (int j = 0; j < 5; j++) {
      arr[i][j]=in.nextInt();
          if (arr[i][j]==1) {
              r=i;c=j;
          }
      }
    }

         if (r==c&&(r==0||r==4))
             counter=4;
         else if(r==c&&(r==1||r==3))
             counter=2;
         else if(r==0&&c==1 || r==1&&c==0 || r==3&&c==4 ||r==4&&c==3)
             counter=3;
         else
    counter=Math.abs(r-c);

    System.out.println(counter);

    }
    }
    */
    
    
    // End  P_A_BeotifulMarix
    //end P_A_BeotifulMatrix
    