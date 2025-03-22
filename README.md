public class myrotate {
    public static void main(String[] args) {
        int[][] matrix = {
            {1, 2, 3,10},
            {4, 5, 6,11},
            {7, 8, 9,12},
            {13,14,15,16}
        };   
        
        int row = matrix.length;
        int column = matrix[0].length;
        for (int i = 0, j = matrix.length - 1; i < j; ++i, --j) {
            int[] temp = matrix[i];
            matrix[i] = matrix[j];
            matrix[j] = temp;
        }
        for (int i = 0; i < row; i++) {
            for (int j = i+1 ; j < column; j++) {
                int temp=matrix[i][j];
                matrix[i][j]=matrix[j][i];
                matrix[j][i]=temp;
            }
        }
        
        
        System.out.println("Transpose:");
        for (int i = 0; i < row; i++) {
            for (int j = 0; j < column; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
