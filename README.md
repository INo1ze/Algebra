# Algebra
Trabajo colabolativo
import java.util.Scanner;
/**
 *
 * @author Diego Lienzo, Angel Morales, Dario Enriquez.
 */
public class Matriz {
    public static void main(String [] args){
        Scanner enter = new Scanner(System.in);
        System.out.println("Numero de filas: ");
        int fil = enter.nextInt();
        System.out.println("Numero de columnas: ");
        int col = enter.nextInt();
        
        MMat matrizOne = new MMat(col, fil);
        
        matrizOne.llenarM();
        matrizOne.impM();
    }
}


public class MMat{
    int col, val, fil, matriz[][];
    int vec [];
    Scanner enter = new Scanner(System.in);
    
    MMat(int col, int fil){
    this.col = col;
    this.fil = fil;
    matriz = new int [fil][col];
}
    MMat(int val){
         this.val = val;
         vec = new int[val];
    }
    public void llenarM(){
        for(int i = 0; i < fil; i+=1){
            for(int j = 0; j < col; j+=1){
                System.out.println("Posición "+"("+(i+1)+"), ("+(j+1)+")");
                matriz[i][j] = enter.nextInt();
            }
        }
    }
        
    public void impM(){
        for(int i = 0; i < fil; i +=1){
            for(int j = 0; j < col; j +=1){
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println("");
        }
        System.out.println("Campos Morales Angel, Lienzo G. Diego, Enriquez B. Dario");
}

}
