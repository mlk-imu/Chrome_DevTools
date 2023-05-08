# DevTools
Привет! Здесь о том, как я училась разбираться в консоли разработчика в рамках интенсива от Школы седого тестировщика)
Это небольшое портфолио собрано из моих домашних заданий.
Тестируемый проект - http://test.it-online-school.ru/

## Оглавление

1. [Вкладки Elements и Console.](эмуляция-мобильных-экранов-вкладки-elements-и-console)
2. [Вкладки Sources и Network.](вкладки-sources-и-network)
3. [Вкладки Performance, Application и Security.](работа-с-производительностью-безопасностью-и-куками-вкладки-performance-application-и-security)

### Эмуляция мобильных экранов. Вкладки Elements и Console.
1. #### Сэмулировать на выбор два мобильных девайса.
![image](https://user-images.githubusercontent.com/97261554/236709646-e1803044-db57-4ae1-8bd1-0cc8669a28e9.png)![image](https://user-images.githubusercontent.com/97261554/236709987-40dff923-4def-4a12-82ed-e9cde5d59c86.png)

2. #### Добавить свой (кастомный) девайс.
![image](https://user-images.githubusercontent.com/97261554/236710201-929141ac-40a2-44c7-81e2-c5a10f907bc6.png)

3. #### Изменить название /html/body/div/div[3]/div[1]/div[1]/div/div[1]/div[1]/div/div/div на "Самая отличная, вкусная, яркая и прекрасная" (Главная страница).
![image](https://user-images.githubusercontent.com/97261554/236710261-a0c21c95-43ee-44bf-88be-b81462e49d02.png)

4. #### Изменить цвет текста на белый #slider-1-layer-6 (Главная страница).
![image](https://user-images.githubusercontent.com/97261554/236710320-80f59cbf-88c4-4fb1-b193-812838e3cdcf.png)

5. #### Получить селекторы XPATH и CSS двух элементов на выбор.
>***Иконка пиццы Маргарита***
>
>**CSS** #rev_slider_1_1 > div.tp-bullets.metis.horizontal > div:nth-child(2) > span.tp-bullet-img-wrap > span
**XPATH** //*[@id="rev_slider_1_1"]/div[4]/div[2]/span[1]/span


>***Лого***
>
>**CSS** #header > div.logo > a > img.logoImage
**XPATH** //*[@id="header"]/div[1]/a/img[1]

6. #### Найти и скинуть лог ошибок в консоли на главной странице.
![image](https://user-images.githubusercontent.com/97261554/236710502-f2ebf281-93b0-479d-bb8a-ce631abea394.png)

7. #### Сделать скриншоты посредством DevTools элемента //*[@id="header"] (Главная страница).
![image](https://user-images.githubusercontent.com/97261554/236710659-6c6c4688-0c1f-4031-82f4-a943f1e6a5ed.png)

_____

### Вкладки Sources и Network.
1. #### Заменить изображение пиццы "Свежесть" любой картинкой из интернета. Изображение должно загружать непосредственно со стороннего сайта. Во вкладке Pages указать сервер, с которого происходит загрузка. http://test.it-online-school.ru/pizzas.html.
![image](https://user-images.githubusercontent.com/97261554/236711046-8d6f5a7d-5aa8-4272-b0b8-0c5f39973db6.png)
![image](https://user-images.githubusercontent.com/97261554/236711129-ea801e0c-f4c6-4bd8-bfb1-dae559932751.png)

2. #### Найти и скинуть cURL запрос для страницы contact.html

>curl "http://test.it-online-school.ru/contact.html" ^
  -H "Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9" ^
  -H "Accept-Language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7" ^
  -H "Cache-Control: no-cache" ^
  -H "Connection: keep-alive" ^
  -H "Cookie: _ym_uid=1671095564669255018; _ym_d=1671095564; _ym_isad=1; _ym_visorc=w" ^
  -H "Pragma: no-cache" ^
  -H "Referer: http://test.it-online-school.ru/contact.html" ^
  -H "Upgrade-Insecure-Requests: 1" ^
  -H "User-Agent: Mozilla/5.0 (iPad; CPU OS 11_0 like Mac OS X) AppleWebKit/604.1.34 (KHTML, like Gecko) Version/11.0 Mobile/15A5341f Safari/604.1" ^
  --compressed ^
  --insecure
  
  3. #### Добавить кастомное ограничение скорости на выбор.
  ![image](https://user-images.githubusercontent.com/97261554/236711235-5afe8884-075b-4666-900f-c9a5edbaf242.png)

  4. #### Определить время ответа от сервера изображения http://test.it-online-school.ru/upload/team.jpg для:
- вашей скорости интернета.
- для быстрого 3G интернета.
В двух вариантах: с включенным и отключенным кешем. Объяснить разницу во времени ответа.

>При моей скорости (Wi-Fi):
>- с выкл кешем 23.96ms
>- с вкл кешем 6.92ms
>
>Быстрый 3G:
>- с выкл кешем 583.98ms
>- с вкл кешем 12.51ms
>
>Чем выше скорость интернета, тем меньше времени 
требуется серверу на обработку запроса. 
Изображения, сохранённые в кеше, загружаются быстрее,
соответственно, время ответа меньше.

5. #### Определить на чьей стороне проблема (клиент или сервер) для следующей ошибки:
На странице Контакты при клике на кнопку "Отправить сообщение" не происходит никаких действий.
Объяснить, почему именно такой ответ.

![image](https://user-images.githubusercontent.com/97261554/236711351-5b22fa40-75f5-4f2d-8a37-0efebadaa479.png)

>Проблема на стороне клиента - ошибка 404. Не указан параметр **action** (путь) и форма не знает, куда ей отправляться)

 6. #### Разобраться, почему нельзя ничего написать в поле Email на странице Контакты.
 ![image](https://user-images.githubusercontent.com/97261554/236711431-73e5d1d4-314a-4955-893d-221ba9e22016.png)
>Поле заблокировано атрибутом **disabled**. Его просто нужно убрать)

_____

### Работа с производительностью, безопасностью и куками. Вкладки Performance, Application и Security.
1. #### Выгрузить статистику по производительности тестового сайта при работе слайдера на главной странице. Замер произвести в течение примерно 15 секунд. Указать на самые ресурсоемкие места.
![image](https://user-images.githubusercontent.com/97261554/236711639-eeed32bc-0042-494b-a0fc-e5ea548982df.png)
![image](https://user-images.githubusercontent.com/97261554/236714671-47c9372a-5658-452f-a164-b46d0f857ff4.png)
>Самые ресурсоемкие места - при смене слайда.

2. #### Взять на выбор два любых сайта и определить безопасность использования (наличие протокола HTTPS). Проанализировать в действительности ли он нужен.

>https://www.wildberries.ru/ - сертификат есть. 
На этом сайте он обязателен, т.к. используются персональные данные 
покупателей, в т.ч. данные платёжных карт.
>
>http://www.bibika.ru/ - сертификата нет. 
На сайте есть форма подачи объявлений, которая требует указания 
персональных данных продавца. Необходим сертификат.

3. #### Определить в каком месте хранится информация о включении/выключении автовоспроизведения на youtube. Указать ключ и значение данного параметра.
![image](https://user-images.githubusercontent.com/97261554/236711926-8503fb5b-0900-4c5b-bcfb-85da2bd99a40.png)

>Информация об автовоспроизведении хранится в локальном хранилище.
>Ключ и значение выделила на скрине. Значение может быть true для выкл автовоспроизведения и false для вкл. В сессионном хранилище эта инф-ция тоже хранится, но только в рамках сессии страницы.

4. #### Объяснить разницу между кешем, локальным хранилищем, сессионным хранилищем и куками. Привести примеры для каждого варианта.
>В кеше сохраняется информация о посещённых сайтах - страницы html, изображения. Это нужно для того, чтобы каждый раз не обращаться к серверу и загрузка происходила быстрее.
>
>В локальном хранилище сохраняется информация, введенная нами на сайте. Например, мы пишем сообщение в диалоге вк, отправить не успели и случайно закрыли браузер. Открыв браузер и вернувшись к диалогу, мы увидим, что сообщение сохранилось и его не нужно вводить заново.
>
>Сессионное - сохраняет всё то же, но по завершении сессии страницы всё очищается из сессионного хранилища.
>
>Куки - данные для общения клиента и сервера. С помощью куки, сайт запоминает пользователя и подстраивается под него) Например, с помощью куки, сайт подкидывает нам рекомендации музыки или товары, которые могут нам понравится.



