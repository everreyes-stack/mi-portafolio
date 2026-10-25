# Guia del Laboratorio 03: Trabajo colaborativo con repositorios remotos

Esta guia explica como colaborar en el proyecto de otra persona sin tocar su repositorio original. Se usa el proyecto tienda-tecsup, una pagina de carrito de compras que tenia un error en el calculo del total. Esta pensada para un companero que nunca vio el proyecto.

## Requisitos

- Equipo con **Windows 11**
- **Git** instalado y configurado
- *Visual Studio Code* como editor
- Cuenta activa en **GitHub** y conexion a Internet

## Pasos de uso

1. Hacer un fork del repositorio del docente con el boton Fork
2. Clonar el fork en la computadora con git clone
3. Reportar el error con un Issue en el repositorio del docente
4. Corregir el error en una rama nueva
5. Subir la rama al fork con git push
6. Abrir un Pull Request hacia el repositorio del docente

### Comandos usados

Antes de empezar comprueba que Git funciona con `git --version`, y despues de clonar revisa el remoto con `git remote -v`.

```bash
git clone https://github.com/everreyes-stack/tienda-tecsup.git
cd tienda-tecsup
git checkout -b fix-total-carrito
git diff
git add script.js
git commit -m "Corrige el calculo del total del carrito (#1)"
git push origin fix-total-carrito
```

### Archivos del proyecto

| Archivo | Para que sirve |
|---------|----------------|
| index.html | La pagina con el titulo, la tabla del carrito y el total |
| estilos.css | Los colores y la tipografia de la pagina |
| script.js | Calcula el total recorriendo los productos |
| README.md | Describe como debe verse la pagina cuando funciona bien |

### El error corregido

El total mostraba S/ 43.00 en lugar de S/ 68.00 porque sumaba el precio sin multiplicarlo por la cantidad. Se cambio la linea `total = total + producto.precio;` por `total = total + producto.precio * producto.cantidad;` en la funcion calcularTotal.

## Mi avance

- [x] Hacer el fork y clonarlo
- [x] Crear el Issue del error del total
- [x] Corregir en la rama fix-total-carrito
- [x] Abrir el Pull Request
- [ ] Sincronizar el fork con Sync fork y git pull

## Captura

![Captura de mi trabajo](../img/captura.png)

## Enlaces

- [Que es un fork en GitHub](https://docs.github.com/es/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks)
- [Volver al README](../README.md)