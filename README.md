# Ejercicio 2 - Despliegue de práctica React

Esta es la práctica del módulo de React desplegada en un servidor AWS, tal como se pide en el ejercicio 2 del módulo de Despliegue en Servidor.

## 🌐 Accesos

- **Acceso vía DNS pública**:  
  http://ec2-100-28-161-187.compute-1.amazonaws.com/login

## 🛠️ Despliegue

- La práctica ha sido compilada con `npm run build`.
- El contenido del directorio `/dist` se ha copiado al servidor EC2.
- El servidor web NGINX está configurado para servir la web desde `/home/ubuntu/build`.
- Se ha configurado `try_files $uri $uri/ /index.html` para soportar rutas con React Router.
- También se ha redirigido el error `404` a `index.html`.

## ✅ Resultado

La aplicación responde correctamente tanto por IP como por DNS. Al acceder al dominio público se visualiza correctamente la práctica de React.