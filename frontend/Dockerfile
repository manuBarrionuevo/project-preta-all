# Utiliza una imagen base oficial de Node.js
FROM node:18-alpine

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia el package.json y package-lock.json al contenedor
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto de los archivos del proyecto al contenedor
COPY . .

# Expone el puerto 5173 (puerto predeterminado de Vite)
EXPOSE 5173

# Comando por defecto para ejecutar la aplicación
CMD ["npm", "run", "dev", "--", "--host"]
