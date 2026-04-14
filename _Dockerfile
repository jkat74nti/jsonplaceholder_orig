# Vi byter från 12 till 20 (LTS) för att stödja modern JavaScript-syntax
FROM node:20-alpine

# Sätt arbetskatalog
WORKDIR /usr/src/app

# Installera json-server globalt (nu kommer den köras på en miljö som förstår ??)
RUN npm install -g json-server

# Kopiera in din databasfil
COPY db.json .

# Exponera porten
EXPOSE 32768

# Viktigt: Använd 0.0.0.0 för att containern ska svara på anrop utifrån
CMD ["json-server", "--watch", "db.json", "--host", "0.0.0.0"]
