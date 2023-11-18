# Игра Pac-Man
## Pac-Man
- Сделать реализацию движения (4 стороны) на кнопки. При нажатии меняется только направление. Пакман движется сам. 
- Пакман может быть абсолютно любой формы, кроме прямоугольника и квадрата, главное правильно переопределить `boundingRect` и `shape` для сложных фигур
## Сцена
- Перед началом игры должна быть возможность создать уровень самому, перетащив все стены, монетки и пакмана с помощью drag and drop механизма.
-	Пакман должен быть только один, тогда как монеток и стен можно разместить сколько угодно или какое-то заданное число, не меньше 10. 
## Стены
-	Стены могут быть просто прямоугольниками, которые можно вращать на сцене, чтобы создавать вертикальные и горизонтальные
## Монетки
-	При соприкосновении с пакманом монетка исчезает со сцены
-	Форма – любая отличная от прямоугольника и квадрата.
## Минимальный интерфейс	
- Представление графической сцены (`QGraphicsView`)
-	Набор фигур для Drag and Drop
-	Кнопка “Начать игру”
-	Кнопка “Стоп”
-	Меню “Справка” с описанием горячих клавиш и особыми правилами (если такие имеются).
-	Счетчик собранных момент
## Геймплей
-	Если пакман сталкивается со стеной, то до момента пока он не отойдет от нее, его цвет должен меняться на другой.	
- Монетки при сборе должны исчезать со сцены и добавляться в счетчик.	
- Игра оканчивается при сборе всех монеток или по кнопке “Стоп”.	
- Если собраны все монетки, выводится поздравительное сообщение.
- Когда игра началась, нельзя добавить новые фигуры или менять положение текущих (кроме перемещения самого пакмана).
- Все столкновения на сцене обрабатываются с помощью методов `QGraphicsScene::collidingItems`, `QGraphicsItem::collidingItems`  и т.д.
