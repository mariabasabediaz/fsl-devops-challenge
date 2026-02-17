# 1. Usamos una imagen ligera de Node.js
FROM node:18-alpine

# 2. Creamos el directorio de trabajo
WORKDIR /app

# 3. Copiamos los archivos de dependencias
COPY package*.json ./

# 4. Instalamos solo lo necesario para producción
RUN npm ci --only=production

# 5. Copiamos el resto del código
COPY . .

# 6. Exponemos el puerto que usa tu app (ajústalo si es necesario, ej: 3000)
EXPOSE 3000

# 7. Comando para arrancar la app
CMD ["npm", "start"]
