# SOLID_shop
Тема: Magics, DRY, SOLID

Задача: Магазин

Пояснения:

Магические числа. Пример - имплементация метода getCount() в [классе OrderImp](https://github.com/bojark/JavaPatternsHomework4/blob/fd526c0d2408f85351f56067d903840f3b6ba162/src/main/java/classes/OrderImp.java#L11). Номер заказа и генерируется, и геттится через методы, а не руками.

DRY. Пример -- реализация интерфейса [ConsoleInterface](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/classes/ConsoleInterfaceImp.java#L1-L33), реализация [списка команд](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/classes/Commands.java) через Enum и доступ к нему по методу [commands()](https://github.com/Dmitry1402/SOLID_shop/blob/2efe24bbab04c06900f8ecadd0d301fb868f58f0/src/classes/Main.java#L80) в Main.

Single Responsibility Principle. Пример -- интерфейсы и асбтрактные классы [Category](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/abstracts/Category.java), [Cart](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/abstracts/Cart.java), [Order](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/abstracts/Order.java) и т.д., методы в имплементации интерфейса Shop. Все отвечают за свою область задач, связаны через интерфейс [Shop](https://github.com/Dmitry1402/SOLID_shop/blob/main/src/abstracts/Shop.java).

Open/Close. Пример -- интерфейсы и абстрактные методы практически для всей фунциональности, protected и private поля у реализаций. Это же может служить и примером принципа Dependency inversion principle: интерфейс Shop и его имплементация за редким исключением ссылаются на интерфейсы.

Принцип Лисков явно не выражен: в принципе, я не стал наследовать Cart от List, хотя функциональность корзины близка к списку как таковому, но сама корзина -- не список, хотя и основана на нём.
