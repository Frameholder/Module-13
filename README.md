# Module-13
ЗАДАНИЕ 13.8.19

Tickets=int(input('Введите количество билетов ')) # задаем количество билетов
Age=[int(input('Введите возраст каждого посетителя ')) for i in range(Tickets)] # просим указать возраст необходимое количество раз, исходя из количества билетов
listMask = [] # задаем список маску, чтобы заменить им исходный список с возрастом, так как каждому значению возраста соответствует свое значение стоимости билета
for i in Age:
    if i<18:
        listMask.append(0) # меняем все что до 18 лет не включая на 0 рублей
    elif 18<=i<25:
         listMask.append(990) # меняем все что от 18 включая до 25 лет не включая на 990 рублей
    else:
         listMask.append(1390) # оставшиеся старше 25 лет включая меняем на 1390 рублей
Final_price=sum(listMask)
if Tickets>=3: # готовим почву для дисконта если билетов больше или равно 3
    print('Общая стоимость билетов c учетом скидки составит',Final_price*0.9,'рублей')
else:
    print('Общая стоимость билетов составит',Final_price,'рублей')






