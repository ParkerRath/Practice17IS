# Practice17IS
# Тестирование сайта отправкой разных данных:  

  
## Сделан первый запрос с валидными данными 

<img width="1876" height="1465" alt="изображение" src="https://github.com/user-attachments/assets/65fab5db-58f3-483d-b37b-5100c8444864" />  

## Сделан второй запрос с невалидными данными 

<img width="1891" height="1517" alt="изображение" src="https://github.com/user-attachments/assets/42fb11ae-3ccb-4f38-9cb4-3716e4d3f166" />  

### Вывод по двум запросам:  
Первое - отсутствие строгой валидации входных данных. При отправке невалидных данных сервер не отклонил запрос с кодом 4xx, а обработал его иначе [уточните: вернул 200, 500 или пустой ответ] — это признак недостаточной серверной валидации.  

Возможное отсутствие rate limiting. Если повторные невалидные запросы не блокируются — риск brute-force.  

### Рекомендации по исправлению:
Ввести схемы валидации для всех эндпоинтов.  
Унифицировать формат ошибок (например, RFC 7807 Problem Details).  
Добавить negative-тесты в CI.  
Отключить verbose-ошибки в production  

# Тестирование сайта наплывом пользователей через Postman:  


<img width="2009" height="978" alt="изображение" src="https://github.com/user-attachments/assets/991f40be-2071-4beb-8788-c4d4af61fb7b" />  

<img width="2025" height="983" alt="изображение" src="https://github.com/user-attachments/assets/e312c6c8-9dae-41e5-aed5-90a69fd166ba" />  

<img width="2014" height="997" alt="изображение" src="https://github.com/user-attachments/assets/a671ddcf-001c-4085-87c7-23386dde8b65" />







