# Pr-ctica3.Utiler-asYClasesDeUsoGeneral
Práctica3. Utilerías Y Clases De Uso General - Hernández Rubio Dana Valeria
EJERCICIO 1
> Realizar un diccionario con 5 palabras usando Hashtable e imprimir todos los elementos.

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package ejerciciospoop3;

import java.util.Enumeration;
import java.util.Hashtable;
import java.util.Calendar;
import java.util.Date;
import java.util.GregorianCalendar;

/**
 *
 * @author Optiplex 780
 */


public class EjerciciosPOOP3 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        System.out.println("Diccionario: ");
        
        Hashtable <String, String> miDiccionario = new Hashtable <String, String>();
        miDiccionario.put("Fonética", "Parte de la lingüística que estudia los sonidos de las lenguas.");
        miDiccionario.put("Desperfecto", "Daño o deterioro de poca importancia que sufre una cosa.");
        miDiccionario.put("Audiovisual", "Que se basa en la utilización conjunta del oído y de la vista, mediante imágenes y sonidos grabados, en especial para elaborar material didáctico o informativo.");
        miDiccionario.put("Sincronización", "Propiciar que dos fenómenos o acciones resulten coincidentes en el tiempo o se organicen según un determinado orden.");            
        miDiccionario.put("Entonación", "Variación del tono de la voz de una persona al hablar; puede indicar algún tipo de matiz expresivo referente al mensaje o a la propia persona.");
        
        String clave;
        String valor;
        Enumeration<String> claves = miDiccionario.keys(); 
        while(claves.hasMoreElements()){
        clave =claves.nextElement();
        valor = miDiccionario.get(clave);
            System.out.println("(Palabra) " + clave + " " + "(Significado) " + valor);
        }
        
    }
}
