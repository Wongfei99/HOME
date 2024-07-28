/* a->ai e->enter i->imes o->ober u->ufat */
import java.util.Scanner;
public class Encriptador {
 public static void main(String[] args) {
 Scanner sc = new Scanner(System.in);
 System.out.println("Elige una opcion");
 System.out.println("Para encriptar escribe : 1");
 System.out.println("Para desencriptar escribe : 2");
 int opcion = sc.nextInt();
 sc.nextLine();
 if (opcion == 1) {
 System.out.println("Ingresa el texto a encriptar");
 String textoOriginal = sc.nextLine();
 String textoEncriptado = encriptarTexto(textoOriginal);
 System.out.println("textoEncriptado = " + textoEncriptado);
 }else if (opcion ==2){
 System.out.println("Ingresa el texto a desencriptar");
 String textoOriginal = sc.nextLine();
 String textoDesencriptado = descencriptarTexto(textoOriginal);
 System.out.println("textoDesencriptado = " + textoDesencriptado);
 }else{
 System.out.println("Opcion no valida");
 }
 }

public static String encriptarTexto(String textoOriginal){
 char[] caracteres = textoOriginal.toCharArray();
 StringBuilder textoEncriptado = new StringBuilder();

 for(char caracter : caracteres){
 switch(caracter){
 case 'a':
 textoEncriptado.append("ai");
break;
 case 'e':
 textoEncriptado.append("enter");
break;
 case 'i':
 textoEncriptado.append("imes");
break;
 case 'o':
 textoEncriptado.append("ober");
break;
 case 'u':
 textoEncriptado.append("ufat");
break;
 default:
 textoEncriptado.append(caracter);
break;
 }

 }

 return textoEncriptado.toString();


}
public static String descencriptarTexto(String textoEncriptado) {
 String textoDesencriptado =textoEncriptado
 .replaceAll("ai","a")
 .replaceAll("enter","e")
 .replaceAll("imes","i")
 .replaceAll("ober","o")
 .replaceAll("ufat","u");
 return textoDesencriptado;
 }
}
