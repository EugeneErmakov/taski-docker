FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install

COPY . .
RUN npm run build

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]
#CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]