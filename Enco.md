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
