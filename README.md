```sudo apt update```
```sudo apt install nginx```
[7:09 PM]
```sudo nano /etc/nginx/sites-available/default```
[7:09 PM]
```server {
    listen 80;
    server_name your_domain_or_IP;

    location / {
        root /var/www/html;
        autoindex on;        # Enables directory listing
        autoindex_exact_size off;  # Show file sizes
        autoindex_localtime on;    # Show file modification times
    }

    # Optionally, you can configure logging
    access_log /var/log/nginx/access.log;
    error_log /var/log/nginx/error.log;
}```
NEW
[7:09 PM]
```sudo mkdir -p /var/www/html```
[7:10 PM]
```sudo chown -R www-data:www-data /var/www/html```
```sudo chmod -R 755 /var/www/html```
[7:10 PM]
```sudo nginx -t```
[7:10 PM]
```sudo systemctl restart nginx```
