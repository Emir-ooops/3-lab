# Отчет по 3 лабе 
## Задание: Сделать, чтобы после пуша в ваш репозиторий автоматически собирался докер образ и результат его сборки сохранялся куда-нибудь.

Для выполнение задания нобходимо создадать в папке .github папку workflows с файлом расширения yml, где юудет записан код с инструкциями для github actions.

![image](https://github.com/Emir-ooops/3-lab/assets/112953051/a6776f1e-2b35-4e8b-9ce0-ef1f62239387) 

Данный скрипт выполняется при каждой загрузке в определенную директорию ветки main (в данном случае мы специально создали папку pushhere для этой цели). Также мы извлекаем секретный токен, который затем передается в Dockerfile

Мы создадим Dockerfile, который будет автоматически создавать новый файл в формате текстового документа при каждом обновлении ветки main нашего репозитория. Этот файл будет сохраняться в специально созданной папке cloud/lab3/pushhere/ и затем загружаться в основную директорию репозитория. Для получения необходимых разрешений мы будем использовать секретный ключ из файла docker-build.yml.

![image](https://github.com/Emir-ooops/3-lab/assets/112953051/8e9dbbe0-8d23-4ada-9247-4449fb305305)

Теперь каждый раз, когда происходит обновление в ветке main, система автоматически проверяет наличие изменений в папке pushhere. Если изменения обнаружены, создается текстовый документ hello.txt с записью "hello". При каждом запуске нашего рабочего процесса мы можем отслеживать прогресс работы во вкладке actions нашего репозитория.

![image](https://github.com/Emir-ooops/3-lab/assets/112953051/11b65d3c-1e3e-474a-900d-967d2ea54933)
