# Algebra
Trabajillo
import java.util.Scanner;
/**
 *
 * @author Diego Lienzo, Angel Campos, Dario Enriquez
 */
public class MMat{
    public static void main(String [] args){
        Scanner enter = new Scanner(System.in);
        System.out.println("Numero de filas: ");
        int fil = enter.nextInt();
        System.out.println("Numero de columnas: ");
        int col = enter.nextInt();
        
        MMat matrizOne = new MMat(col, fil);
        
        matrizOne.autors();
        
        MMat matrizTwo = new MMat(col,fil);
        
        matrizTwo.llenarM();
        }
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
        
   public void autors()
   {
       System.out.println("Campos Morales Angel, Lienzo G. Diego, Enriquez Dario");
   }
    public void impM(){
        for(int i = 0; i < fil; i +=1){
            for(int j = 0; j < col; j +=1){
                System.out.print(matriz[i][j] + " ");
            }
            System.out.println("");
        }
}

}

