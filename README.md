# charkavyuh-spiral-matrix-codevita-
in java


import java.util.*;
import java.lang.*;

public class HelloWorld
{

     public static void main(String []args)
     {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int size1=((n*n)/11)+1;
        int[][] arr1=new int[size1][2];
        arr1[0][0]=0;
        arr1[0][1]=0;
        int[][] arr=new int[n][n];
        int count=1;
        int pop=0;
        int a=1;
        int size=n-1;
        for(int w=0;w<=n/2;w++)
        {
            int i=w,j=w;
            if(j==size-w)
             {
               arr[i][j]=count;
              }
            for(j=j;j<size-w;j++)
            {
             
                arr[i][j]=count;
                if(count%11==0)
                {
                    arr1[a][0]=i;
                    arr1[a][1]=j;
                    a++;
                }
                if(count==n*n)
                {
                    pop++;
                    break;
                }
                count++;
                
            }
            if(pop>0)
            {
                break;
            }
            //j=j+1;
            for(i=i;i<size-w;i++)
            {
                arr[i][j]=count;
                if(count%11==0)
                {
                    arr1[a][0]=i;
                    arr1[a][1]=j;
                    a++;
                }
                if(count==n*n)
                {
                    pop++;
                    break;
                }
                count++;
            }
            if(pop>0)
            {
                break;
            }
            for(j=j;j>0+w;j--)
            {
                arr[i][j]=count;
                if(count%11==0)
                {
                    arr1[a][0]=i;
                    arr1[a][1]=j;
                    a++;
                }
                if(count==n*n)
                {
                    pop++;
                    break;
                }
                count++;
            }
            if(pop>0)
            {
                break;
            }
            //j=j-1;
            for(i=i;i>0+w;i--)
            {
                arr[i][j]=count;
                if(count%11==0)
                {
                    arr1[a][0]=i;
                    arr1[a][1]=j;
                    a++;
                }
                if(count==n*n)
                {
                    pop++;
                    break;
                }
                count++;
            }
            if(pop>0)
            {
                break;
            }
        }
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                System.out.print(arr[i][j]+" ");
            }
            System.out.println();
        }
     }
}
