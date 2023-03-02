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

## Задание №6
Найдите полный пусть до файла any.hpp внутри библиотеки boost

realpath any.hpp
![image](https://user-images.githubusercontent.com/116309607/222500472-30dea81f-9765-4a3f-b582-c32983e8471c.png)

## Задание №7
Выведите в консоль все файлы, где упоминается последовательность boost::asio

grep -lr boost::asio
![image](https://user-images.githubusercontent.com/116309607/222500642-09b6b200-b4f9-424b-a63c-42dee4a4d5f4.png)


## Задание №8
Скомпилирутйе boost

./bootstrap.sh --prefix=boost_output

./b2 install
![image](https://user-images.githubusercontent.com/116309607/222500846-90ddcab7-5b8b-469e-a693-3137903b21ec.png)

## Задание №9
Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию ~/boost-libs

mkdir ~/boost-libs

mv * ~/boost-libs
![image](https://user-images.githubusercontent.com/116309607/222501037-3d6a8f3e-cf8e-4cb6-a016-1024f4ffb49b.png)

## Задание №10
Подсчитайте сколько занимает дискового пространства каждый файл в этой директории

cd ~/boost-libs/

ls -sh
![image](https://user-images.githubusercontent.com/116309607/222501254-29769a9f-bc49-4247-91e9-cfee96162ea1.png)

## Задание №11
Найдите топ10 самых "тяжёлых"

find . -type f -exec du -h {} +|sort -rh | head -n 10
![image](https://user-images.githubusercontent.com/116309607/222501574-6b6c3740-3fb0-4cb5-b0ed-273cf6f95326.png)
