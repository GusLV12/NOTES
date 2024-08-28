# Comandos básicos de Linux

1. **`ls`**: Muestra una lista de los archivos y carpetas en el directorio actual.
2. **`cd`**: Permite cambiar de directorio. Por ejemplo, **`cd /home/user`** cambiará el directorio actual al directorio del usuario.
3. **`mkdir`**: Crea un nuevo directorio. Por ejemplo, **`mkdir new_directory`** creará un nuevo directorio llamado "new_directory".
4. **`cp`**: Copia un archivo o directorio. Por ejemplo, **`cp file.txt /home/user/`** copiará el archivo "file.txt" al directorio del usuario.
5. **`mv`**: Mueve o renombra un archivo o directorio. Por ejemplo, **`mv file.txt new_file.txt`** renombrará el archivo "file.txt" a "new_file.txt".
6. **`rm`**: Elimina un archivo o directorio. Por ejemplo, **`rm file.txt`** eliminará el archivo "file.txt".
7. **`sudo`**: Ejecuta un comando como superusuario. Por ejemplo, **`sudo apt-get update`** actualizará el sistema.
8. **`grep`**: Busca en un archivo o en la salida de otro comando por una cadena de texto específica. Por ejemplo, **`grep "search term" file.txt`** buscará el término "search term" en el archivo "file.txt".
9. **`chmod`**: Cambia los permisos de un archivo o directorio. Por ejemplo, **`chmod 755 file.txt`** dará permisos de lectura, escritura y ejecución al propietario del archivo, y solo permisos de lectura y ejecución a otros usuarios.
10. **`top`**: Muestra una lista de los procesos en ejecución y su uso de recursos.
11. **`pwd`**: Muestra la ruta del directorio de trabajo actual.
12. **`cat`**: Se utiliza para visualizar el contenido de un archivo.
13. **`cat > nombredearchivo`**: Crea un nuevo archivo.

## Alias

```bash
echo "Fecha y hora es: "$(date +%d/%m/%Y-%H:%M:%S) >> Fechas.txt
alias consultar_tiempo='echo "Fecha y hora es: "$(date +%d/%m/%Y-%H:%M:%S) >> Fechas.txt'
```

## Comprimiendo y Descomprimiendo archivos

```bash
Comprimir: tar -czvf carpeta_comprimido.tar.gz archivo_carpeta

Descomprimir: tar -xzvf archivo_comprimido.tar.gz
```
