server {
    listen 3000;
    server_name _;
    root /var/www/web2.com/public_html;
    index index.php index.html index.htm;
    location / {
        try_files $uri $uri/ =404;
    }
    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/run/php/php8.1-fpm.sock;
    }
    location ~ /\.ht {
        deny all;
    }
}
