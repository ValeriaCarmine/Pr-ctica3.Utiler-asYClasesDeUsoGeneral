> Realizar una agenda con 5 registros guardando nombre de persona y su cumpleaños usando Hashtable y calendar e imprimir todos los elementos.

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package ejercicio2poop3;

import java.text.DateFormat;
import java.util.Date;
import java.util.Hashtable;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;


/**
 *
 * @author Optiplex 780
 */
public class Ejercicio2POOP3 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        System.out.println("-------------Agenda------------- ");
    Hashtable dates = new Hashtable();
    DateFormat df = DateFormat.getDateInstance();
    dates.put("Dana Hernandez Rubio",new Date(01,11,20)); 
    dates.put("Jessi Bluu Vital",new Date(01,07,9));
    dates.put("Valeria Garcia Torres ",new Date(95,31,30));
    dates.put("Norma Rubio Aranda",new Date(76,01,5));
    dates.put("Scarlett Hernandez Rubio",new Date(96,03,4));
    
    
    Set s = dates.entrySet();
    Iterator e = s.iterator();
    
        while(e.hasNext()){
            Map.Entry aux = (Map.Entry)e.next();
            Object clave = aux.getKey();
            Object cumpleños = aux.getValue();
            
            System.out.print("*Nombre* "+clave);
            System.out.print(" *Cumpleaños* "+ df.format(cumpleños) + "\n");

        }
    }
    
}
