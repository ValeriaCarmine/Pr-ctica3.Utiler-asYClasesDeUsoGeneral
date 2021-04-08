/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package poop3;

import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Calendar;
import java.util.Date;
import java.util.Enumeration;
import java.util.Hashtable;

/**
 *
 * @author Optiplex 780
 */
public class POOP3 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        /**********************Arreglos********************************/
      int[] nums;
      int nums1[];
        
      nums= new int[5]; 
      int[] nums2 = {1,2,3,4,5};
        /**********************for********************************/
        System.out.println("*******************for*************************");
        //for (int i = 0; i < 10; i++) {}
        for (int i = 0; i < nums2.length; i+=2) {
            int j = nums2[i];
            System.out.println(j);
        }
        /**********************for-each********************************/
        System.out.println("*******************for-each************************");
        for (int j: nums2) {
                System.out.println(j);        
        }
        System.out.println("*******************Manejo de Cadenas************************");
        String s= new String("Hola Mundo");
        System.out.println(s);
        String s1 = "Hola Mundo 2";
        System.out.println(s1);
        
        System.out.println("*******************Operador Punto************************");
        
        System.out.println("nums2 lengh = " + nums2.length);
        System.out.println("s lengh = " + s.length());
        System.out.println("s1 lengh = " + s1.length());
        
        System.out.println("*******************Concatenar************************");
        
        String nombre = "Dana";
        String apellido = "Hernandez";
        String nombreCompleto = nombre + " " + apellido;
        System.out.println(nombreCompleto);
        
        System.out.println("*******************Wrapper y Autoboxing************************");
        
        Integer k = new Integer(22);
        Integer l = 22;
        int r = 2 + l;
        System.out.println(r);
       
        String entero = l + "";
        String entero1 = l.toString();
        System.out.println(entero1);
        
        //String entero2 = r.;
        System.out.println("");
        
        System.out.println("*******************Colecciones************************");
        System.out.println("*******************Array-List************************");
        ArrayList<Integer> miArrayList = new ArrayList<Integer>();
        miArrayList.add(50);
        miArrayList.add(22);
        for (Integer elemento : miArrayList) {
            System.out.println(elemento);
        }
        System.out.println("-------------------------------------");
        miArrayList.add(0, 3);
        miArrayList.add(2, 99);
        for (Integer elemento : miArrayList) {
            System.out.println(elemento);
        }
        System.out.println("Tamaño ArrayList" + miArrayList.size());
        System.out.println("Elemento 2 " + miArrayList.get(2));
        
        System.out.println("*******************Hash-Table************************");
        Hashtable<String,Integer> miTabla = new Hashtable<String,Integer>(); 
        miTabla.put("uno", 1);
        miTabla.put("dos", 2);
        miTabla.put("cinco", 5);
        
        System.out.println("¿La tabla tiene el valor siete? " + miTabla.containsKey("siete"));
        System.out.println("El Tamaño de mi tabla es: " + miTabla.size());
        
        for (Integer valor : miTabla.values()) {
            System.out.println(valor);
        }
        
        for (String clave : miTabla.keySet()) {
            System.out.println(clave);
        }
        System.out.println("*******************Enumeracion************************");
        
        String clave;
        Integer valor;
        
        Enumeration<String> claves = miTabla.keys();
        
        while(claves.hasMoreElements()){
            clave = claves.nextElement();
            valor = miTabla.get(clave);
            System.out.println("Clave: " + clave + " Valor: " + valor);
        }
        System.out.println("*******************Math************************");
        
        System.out.println(Math.pow(3,2));
        System.out.println(Math.sqrt(9));
        System.out.println(Math.PI);
        
        System.out.println("*******************Date************************");
        Date hoy = new Date();// fecha de hoy
        System.out.println(hoy);
        
        System.out.println("*******************Calendario************************");
        Calendar calendarioHoy = Calendar.getInstance();
        System.out.println(calendarioHoy);
        
        SimpleDateFormat formatoFecha = new SimpleDateFormat("u-dd-MM-yy");
        System.out.println(formatoFecha.format(hoy));
        String fechaActual = "Hoy es el día ";
            fechaActual += calendarioHoy.get(Calendar.DAY_OF_MONTH)+ " del mes ";
            fechaActual += calendarioHoy.get(Calendar.MONTH)+ " del AÑO ";
            fechaActual += calendarioHoy.get(Calendar.YEAR);
            
         System.out.println("Fecha de hoy");
         System.out.println(fechaActual);
    }
    
}
