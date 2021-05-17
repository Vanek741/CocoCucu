# Первое задание

Задание: Выбрать из первого файла 40 последних строк и записать во второй файл. Записать первые десять строк из второго файла в третий файл. Выбрать во втором файле все строки, содержащие "коко", заменить в этих строках "коко" на "куку" и дозаписать только первые три вхождения в третий файл.

tail -n 40 firstFile.txt > secondFile.txt && head -n 10 secondFile.txt > thirdFile.txt // Выбираем
sed -r 's/coco/cucu/g' secondFile.txt | grep 'cucu' | head -n 3 >> thirdFile.txt // Меняем
sort thirdFile.txt | uniq -c | cat > thirdFile.txt // Выводим
