# web-servers-hw-15

Задание 1:
Установите и настройте Nginx. Создайте html-страничку, где будет указана
ваша фамилия и тема урока. Настройте конфигурацию nginx для отображения
страницы по ссылке http://tms.by

```
server {
        listen 80;
        server_name tms.by;
        root /var/www/tms.by/;
        index index.html;
}    
```

<img width="303" height="268" alt="изображение" src="https://github.com/user-attachments/assets/2777978d-5b8e-43c5-9acf-a24498d45ff6" />

Задание 2 (опционально)
Настройте связку Nginx + Apache. Nginx выступает в качестве reverse proxy.

```
server {
	listen 80;
	server_name tms.by;
	root /var/www/tms.by;
	index index.php;

	location / {
		proxy_pass http://127.0.0.1:8080;
	}
}

```
<img width="557" height="59" alt="изображение" src="https://github.com/user-attachments/assets/248607f5-469e-4059-8f0b-ea2142d76d48" />

