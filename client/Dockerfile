From node:alpine

workdir '/app'

copy ./package.json ./
run npm install
copy . .
run npm run build

From nginx
Expose 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
copy --from=0 /app/build /usr/share/nginx/html