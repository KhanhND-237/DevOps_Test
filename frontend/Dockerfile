FROM node:18 as build
WORKDIR /app
COPY . .
RUN npm install && npm run build --prod

FROM nginx:alpine
COPY --from=build /app/dist/frontend/browser /usr/share/nginx/html
#CMD ["npx", "http-server", "dist"]
EXPOSE 80
