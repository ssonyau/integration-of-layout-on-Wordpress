# Як із зверстаної сторінки створити тему на Wordpress

#### 1) Для початку відкрийте Wordpress, перейдіть до Параметри-Читання та зробіть одну зі сторінок головною. Це дозволить не шукати редаговану сторінку за потреби. В налаштуваннях оберить Статичну сторінку та збережіть зміни.

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-24%20135451.png)

#### 2) Візьміть архів із готовою версткою та розпакуйте його на робочому столі.

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-24%20140904.png)

#### 3) Скачайте порожню тему lesson з https://underscores.me/ , встановіть, активуйте і використовуйте як заготівлю. Після повертаємося до нашого Wordpress і завантажуємо тему(zip. архів), яку ми щойно завантажили, та активуем її. 

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-24%20142103.png)

#### 4) Після заходимо подивитися та бачимо, що тема справді дуже базова і там нічого зайвого немає.

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-24%20143835.png)

#### 5) Скопіюйте всі файли з вашої верстки до папки теми (крім html-файлів). Для цього відкриваємо нашу папку з темою і наш zip.архів, і з zip.архіву переносимо наші стилі, картинки та шрифти до папки. 

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-24%20145052.png)

#### 6) Виберіть у темі HTML-файл шаблону, який хочете змінити. Цілком замініть його вміст кодом з html-файлу. Для цього відкриваємо нашу папку з темою і знаходимо шаблон сторінки, у нас це page.php. Видаляємо все звідси, та вставляємо наш html-код з файлу index.html в файл page.html. 
Виглядати це буде ось так:

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-25%20114849.png) 

#### 7) Після копіювання коду в шаблон сайт втратить шляхи до файлів стилів, картинок і скриптів. Відновіть шляхи, додавши перед адресою код:
```
<?php bloginfo('template_directory') ?>
```
![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-25%20121328.png) 

#### І теж саме робимо в кінці нашого файлу, щоб підключити скріпти:

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-25%20122633.png) 

#### І також підключаємо картинки таким самим способом.

#### Після цього ми можемо зайти, оновити нашу сторінку та побачити, що у нас все підключилося та завантажилося так, як потрібно.

![](https://github.com/ssonyau/integration-of-layout-on-Wordpress/blob/main/Screenshot%202023-04-25%20124725.png) 
 
#### 8) Так як у нас все лежить в одному файлі page.php, це не правильно, нам потрібно перенести наш header та footer в окремі файли. Після перенесення у файлі page.php на місце header та footer вставляємо код:
```
<?php get_header(); ?> 
```
```
<?php get_footer(); ?> 
```

#### Таким чином ми можемо зробити з нашої верстки тему на Wordpress.
