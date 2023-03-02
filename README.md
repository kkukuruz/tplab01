# tplab01
tp-labs 01
## Задание №1
Загрузите boost с помощью утилиты wget

wget https://sourceforge.net/projects/boost/files/boost/1.72.0/boost_1_72_0.tar.gz
![image](https://user-images.githubusercontent.com/116309607/222498633-5224ba9e-1bcf-4a1c-a2bc-cb4776888802.png)

## Задание №2
Разархивируйте скачанный файл в директорию

tar -xf boost_1_72_0.tar.gz
![image](https://user-images.githubusercontent.com/116309607/222499256-cd1e8549-7f6a-48b4-b8a1-321befbd9168.png)

## Задание №3
Подсчитайте количество файлов в директории не включая вложенные директории

cd boost_1_72_0
tree -L 1
![image](https://user-images.githubusercontent.com/116309607/222499562-e8b8f8fd-dd78-425a-b65f-8e1b234091f9.png)


## Задание №4
Подсчитайте количество файлов в директории включая вложенные директории

tree
![image](https://user-images.githubusercontent.com/116309607/222499849-a75711ff-7fdd-46e6-9e8e-49b1e89a2c83.png)

## Задание №5
Подсчитайте количество заголовочных файлов, файлов с расширением .cpp, сколько остальных файлов (не заголовочных и не .cpp)

find . -name "*.cpp" | wc -l
find . -not -name "*.cpp" | wc -l
![image](https://user-images.githubusercontent.com/116309607/222500003-24824e6e-ec1d-464a-8a49-0c3feb157274.png)


