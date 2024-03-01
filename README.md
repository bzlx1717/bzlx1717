import java.util.Random;

public class Maximum
{
    public static int maxima(int [] array)
    {
        int m = 0;
        int i=1;
        while ( i < array.length)
        {
            if (array[i] > array[m])
            {
                m = i;
            }
            i++;
        }
        return m;
    }
    public static int maximum(int [] array)
    {
        int temmaximum = array[0];
        int i=1;
        while ( i < array.length)
        {
            if (array[i] > temmaximum)
                temmaximum = array[i];
            i++;
        }

        return temmaximum;
    }
    public static int minimum(int [] array){
        int temminimum = array[0];
        int i=1;
        while( i < array.length){
            if(array[i] < temminimum)
                temminimum = array[i];
            i++;
        }
        return temminimum;
    }
    public static int minima(int [] array){
        int m = 0;
        int i=1;
        while ( i < array.length)
        {
            if (array[i] < array[m])
            {
                m = i;
            }
            i++;
        }
        return m;
    }

    static int count = 0;
    static boolean compare(int x, int y)
    {
        count++;
        return x > y;
    }
//    public static int [] extremal(int [] array){
//
//        if(array.length==0) return null;
//        int max=array[0];
//        int min=array[0];
//        int i=1;
//        while(i < array.length){
//            if(compare(min,array[i])){
//                min = array[i];
//            }
//            if(compare(array[i],max)){
//                max = array[i];
//            }
//            i++;
//        }
//        return new int []{max,min};
//    }//5

//    static int stringcompre(String x, String y)
//    {
//        count++;
//        return x.compareTo(y);
//    }
//    public static String [] extremal(String [] array){
//
//        if(array.length==0) return null;
//        String max=array[0];
//        String min=array[0];
//        int i=1;
//        while(i < array.length){
//            if(stringcompre(min,array[i])>0){
//                min = array[i];
//            }
//            if(stringcompre(max,array[i])<0){
//                max = array[i];
//            }
//            i++;
//        }
//        return new String []{min,max};
//    }//13 14

    static int  maximum(int [][] x){
        int maxn = maximum(x[0]);
        int i=1;
        while(i < x.length){
            if(maxn<maximum(x[i])){
                maxn = maximum(x[i]);
            }
            i++;
        }
        return maxn;
    }
    // test driver
    public static void main(String[] args)
    {
        int [] arr = new int[]{342,34,233,456};
//        System.out.println(maximum(arr));
//        System.out.println(maxima(arr));

//        System.out.println(minimum(arr));
//        System.out.println(minima(arr));

//        int [] ans = extremal(arr);
//        System.out.println("max: " + ans[0]);
//        System.out.println("min: " + ans[1]);
//        System.out.println("count: " + count);

//        for(int j=1;j<=10;j++){
//            int N = 1000000*j;
//            int [] a = new int[N];
//            Random r = new Random();
//            for(int i=0;i<N;i++){
//                a[i] = r.nextInt();
//            }
//            long t0 = System.currentTimeMillis();
//            maximum(a);
//            long t1 = System.currentTimeMillis();
//            System.out.println(N + " " + (t1-t0));
//        }

//        count=0;
//        String [] twoends = extremal(new String[]{"Zhang", "Li", "Chao", "1", "%", "*", "@"});
//        System.out.println("min=" + twoends[0] + ", and max=" + twoends[1] + ", #comparisons=" + count);

        int [][] arr1 = new int[][]{{342,34,233,456},{123,23,1,567}};
        System.out.println(maximum(arr1));
    }
}
