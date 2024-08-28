# Nmap

### Documentación

- [Guía de referencia de Nmap (Página de manual)](https://nmap.org/man/es/index.html)
- [Nmap Summary (ESP) | HackTricks](https://book.hacktricks.xyz/generic-methodologies-and-resources/pentesting-network/nmap-summary-esp)
- [Qué es Nmap y cómo usarlo: Un tutorial para la mejor herramienta de escaneo de todos los tiempos](https://www.freecodecamp.org/espanol/news/que-es-nmap-y-como-usarlo-un-tutorial-para-la-mejor-herramienta-de-escaneo-de-todos-los-tiempos/)

## Comandos Necesarios

![Nmap Example](/public/img/Kali/nmap-desc.png)

![Nmap Output](/public/img/Kali/nmap-out.png)

### Ejemplo de Uso

```bash
nmap -p- -sVC -sC --open -sS -vvv -n -Pn 10.0.2.4
```
