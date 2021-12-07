# GTCalc

package edu.gatech;

import java.util.Arrays;

public class Main {




    public static void main(String[] args) {

        for (int[] row : convertMap(5))
            System.out.println(Arrays.toString(row));



    }


    public static int[][] convertMap(int v)
    {
        int vertices;
        vertices = v;
        int[][] multi = new int[vertices][vertices];

        for (int i = 0; i < vertices; i++)
        {
            for (int j = 0; j < vertices; j++)
            {
                multi[i][j] = (int) (Math.random() * 2);
            }
        }

        for (int i = 0; i < vertices; i++)
        {
            multi[i][i] = 0;
        }

        for (int i = 0; i < vertices; i++)
        {
            for (int j = 0; j < vertices; j++)
            {
                multi[i][j] = multi[j][i];
            }
        }
        return multi;
    }

}
