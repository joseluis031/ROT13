# ROT13

El link de este repositorio es el siguiente: [GitHub](https://github.com/joseluis031/ROT13.git)

## Codigo de ROT13

```
def descifrar_rot13(texto_cifrado):
    # Inicializamos una cadena vacía para almacenar el texto descifrado
    texto_descifrado = ""
    
    # Iteramos sobre cada caracter en el texto cifrado
    for char in texto_cifrado:
        # Verificamos si el caracter es una letra del alfabeto
        if char.isalpha():
            # Verificamos si el caracter es una letra minúscula
            if char.islower():
                # Aplicamos ROT13 a las letras minúsculas
                # Convertimos el caracter a su valor ASCII, le restamos el valor ASCII de 'a'
                # Sumamos 13 para realizar la rotación, tomamos el resto de la división por 26
                # y luego sumamos el valor ASCII de 'a' nuevamente para obtener el caracter descifrado
                texto_descifrado += chr(((ord(char) - ord('a') + 13) % 26) + ord('a'))
            else:
                # Si el caracter es una letra mayúscula, aplicamos ROT13 de manera similar
                texto_descifrado += chr(((ord(char) - ord('A') + 13) % 26) + ord('A'))
        else:
            # Si el caracter no es una letra del alfabeto, lo dejamos sin cambios
            texto_descifrado += char
    
    # Retornamos el texto descifrado
    return texto_descifrado

texto_cifrado = "Yn fvthvragr vasbeznpvba rf pbasvqrapvny. Gr nlhqnen n cebfrthve ra yn vairfgvtnpvba. Ab gr pbasvrf, ab gbqnf ynf vasbeznpvbarf qr ynf dhr qvfcbarzbf fba gna snpvyrf pbzb rfgn ebgnpvba qr pnenpgrerf. Sveznqb: ha nzvtb. synt{rfgnzbf_rzcrmnaqb_n_pbabpre_nytb_qr_uvfgbevn}"

texto_descifrado = descifrar_rot13(texto_cifrado)

print("Texto descifrado:", texto_descifrado)

```
## Mensaje descifrado usando ROT13

![image](https://github.com/joseluis031/ROT13/assets/91721888/9fceeded-5022-4199-852e-6686f124f93f)
