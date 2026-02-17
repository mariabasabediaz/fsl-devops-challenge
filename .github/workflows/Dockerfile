# 1. Usamos una imagen ligera de Node.js
FROM node:18-alpine

# 2. Creamos el directorio de trabajo
WORKDIR /app

# 3. Copiamos los archivos de dependencias
# (El asterisco ayuda a que si no existe el lock file, no explote)
COPY package*.json ./

# 4. Instalamos las dependencias (usamos install para evitar el error del lock file)
RUN npm install --production

# 5. Copiamos el resto del código del proyecto
COPY . .

# 6. Exponemos el puerto (por defecto 3000 para Node)
EXPOSE 3000

# 7. Comando para arrancar la app
CMD ["npm", "start"]
