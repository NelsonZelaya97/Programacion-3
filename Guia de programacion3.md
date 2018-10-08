# Programacion-3
Repositorio para la materia de Programación 3

//1. Diseñe un algoritmo que imprima en orden descendente 3 números leídos.  

 

package programa1.pkg0; 

  

import javax.swing.JOptionPane; 

  

/** 

* 

* @author Nelson 

*/ 

public class Programa10 { 

  

    /** 

     * @param args the command line arguments 

     */ 

    public static void main(String[] args) { 

        // TODO code application logic here 

            float[ ] a = new float[3];//Arreglo que contendra los numeros ingresados 

    String primerNumero, segundoNumero, tercerNumero;//Variables obtendran los numeros ingresados 

    primerNumero = JOptionPane.showInputDialog("Digite el primer número: " ); 

    segundoNumero = JOptionPane.showInputDialog("Digite el segundo número: " ); 

    tercerNumero = JOptionPane.showInputDialog("Digite el tercer número: " ); 

 

 

 

    //Se pasan los valores 

 

    a[0] = Float.parseFloat(primerNumero); 

    a[1] = Float.parseFloat(segundoNumero); 

    a[2] = Float.parseFloat(tercerNumero); 

    //Se imprimen en orden descendente 

     System.out.println("Orden descendente:"); 

          ordSelDesc(a); 

            for (float num : a) { 

             System.out.println(num); 

        } 

     

} 

  

    private static void ordSelDesc(float[] a) { 

         

    } 

     

} 

 

 

 

 

//2. Escriba un algoritmo que obtenga la suma e imprima además los términos de la siguiente serie:  

  

//2, 5, 7, 10, 12, 15, 17, ..., 1800  

 

 

 

 

 package programa2.pkg0; 

  

/** 

* 

* @author Nelson 

*/ 

public class Programa20 { 

  

    /** 

     * @param args the command line arguments 

     */ 

    public static void main(String[] args) { 

        // TODO code application logic here 

        int i = 2;//Se incia el primer numero de la secuencia 

        int sum = 0;//Se inicializa la suma 

        String band = "T";//Variable que ayudara a comparar 

         

 

 

//Inicio de impresion y suma 

        while (i <=1800){ 

        sum = sum + i;  

        System.out.print(i); 

        System.out.print("\n"); 

//Se compara la variable   

        if( "T".equals(band)){ 

            i = i + 3; 

            band = "F"; 

        } else { 

            i = i +2; 

            band = "T"; 

        } 

        } 

        //Impresion de la suma 

        System.out.print(sum); 

         

        System.out.print("\n"); 

    } 

     

} 

 

 

 

 

//3. Diseñe un algoritmo que dados el peso y la altura de N personas que pertenecen a un departamento de la república; obtenga el promedio del peso y de la altura de esta población.  

 

package programa3.pkg0; 

  

import javax.swing.JOptionPane; 

  

/** 

* 

* @author Nelson 

*/ 

public class Programa30 { 

 

  

    /** 

     * @param args the command line arguments 

     */ 

    public static void main(String[] args) { 

        // TODO code application logic here 

         //Variables para ingresar los datos 

        int nPersonas;//Cantidad de personas 

        float[ ] PersonasPeso;//Peso de personas 

        PersonasPeso = new float[1000]; 

 

 

 

        float[ ] PersonasAltura;//Altura de personas 

        PersonasAltura = new float[1000]; 

        float acu = 0;//Acumulador para promediar peso 

        float acu1 = 0;//Acumulador para promediar altura 

        String NumPersonas, Peso, Altura; 

 

//Variables obtendran los numeros de personas peso y altura 

        NumPersonas = JOptionPane.showInputDialog("Digite la cantidad de personas: " ); 

        nPersonas = Integer.parseInt(NumPersonas); 

        for (int i = 0; i < nPersonas;i++){ 

        //SE obtienen datos de peso y altura 

        Peso = JOptionPane.showInputDialog("Digite el peso (En Libras): " ); 

        PersonasPeso[i] = Float.parseFloat(Peso); 

        acu = acu + PersonasPeso[i]; 

        Altura = JOptionPane.showInputDialog("Digite la altura de personas (En metros): " ); 

        PersonasAltura[i] = Float.parseFloat(Altura); 

        acu1 = acu1 + PersonasAltura[i]; 

        } 

       

 

  //Se imprimen los promedios 

        JOptionPane.showMessageDialog(null, "El promedio de peso es: " + acu/nPersonas,null, JOptionPane.INFORMATION_MESSAGE ); 

        JOptionPane.showMessageDialog(null, "El promedio de altura es: " + acu1/nPersonas,null, JOptionPane.INFORMATION_MESSAGE ); 

    } 

     

} 

 

 

 

//4. Una tienda ha puesto en oferta la venta de un producto, ofreciendo 15% de descuento por la compra de 3 docenas y 10% en caso contrario. Además por la compra de más de 3 docenas se obsequia una unidad por cada docena en exceso sobre 3. Diseñe un programa que determine el monto de la compra, el monto de descuento y el número de unidades de obsequio para cada uno de los 10 clientes que se atendieron en el día.  

 

package programa4.pkg0; 

  

import java.util.Scanner; 

  

/** 

* 

* @author Nelson 

*/ 

 

 

public class Programa40 { 

  

    /** 

     * @param args the command line arguments 

     */ 

    public static void main(String[] args) { 

        // TODO code application logic here 

            int a=0,n,ob=0,par; 

        double precio,totc,des,s; 

        Scanner teclado =new Scanner(System.in); 

        System.out.println("Ingrese la cantidad de docenas:"); 

        n=teclado.nextInt(); 

        System.out.println("Ingrese el precio:"); 

        precio=teclado.nextDouble(); 

        if(n==3){ 

            s=n*precio; 

            des=s*0.15; 

            totc =s-des; 

             

        } 

        else{ 

            s=n*precio; 

            des=s*0.10; 

            totc =s-des; 

         

 

 

 

    for(int i=4;i<=n;i++){ 

            if(n>3){ 

                ++ob; 

            } 

            } 

            a=n+ob; 

        } 

        System.out.println("total de compra es: "+totc); 

        System.out.println("descuento: "+des); 

        System.out.println("unidades de regalo: "+ob); 

  

    } 

     

} 

//5. Una compañía dedicada al alquiler de automóviles cobra $30.00 hasta un máximo de 300 Km de distancia recorrida. Para más de 300 y hasta 1000 Km cobra $30.00 más un monto adicional de $0.15 por cada Kilómetro en exceso sobre 300. Para más de 1000 Km cobra $30 más un monto de $0.10 por cada Kilómetro en exceso de 1000. Diseñe un programa que calcule el monto a pagar por cada automóvil cobrado en un día de trabajo. 

 

package programa5.pkg0; 

  

import java.util.Scanner; 

 

 

 

  

/** 

* 

* @author Nelson 

*/ 

public class Programa50 { 

  

    /** 

     * @param args the command line arguments 

     */ 

    public static void main(String[] args) { 

        // TODO code application logic here 

                int kil; 

        double ex=0,tot=0; 

        Scanner teclado=new Scanner(System.in); 

        System.out.println("Ingrese su el numero de kilometros recocorridos"); 

        kil=teclado.nextInt(); 

        if(kil>=300 && kil<=1000){ 

            ex =(kil-300)*0.15; 

            tot =ex+30; 

        } 

        if(kil>1000){ 

            ex= (kil-1000)*0.10; 

            tot= ex+30; 

        } 

        System.out.println("Total a pagar: "+tot); 

  

    } 

     

} 
