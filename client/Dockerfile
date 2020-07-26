From node:alpine

workdir '/app'

copy ./package.json ./
run npm install
copy . .
run npm run build

From nginx
Expose 3000
COPY ./Nginx/default.conf /etc/Nginx/conf.d/default.conf
copy --from=0 /app/build /usr/share/nginx/html