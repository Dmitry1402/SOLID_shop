# SOLID_shop
Тема: Magics, DRY, SOLID

Задача: Магазин

Пояснения:

Магические числа. Пример - имплементация метода getCount() в классе OrderImp(https://github.com/bojark/JavaPatternsHomework4/blob/fd526c0d2408f85351f56067d903840f3b6ba162/src/main/java/classes/OrderImp.java#L11). Номер заказа и генерируется, и геттится через методы, а не руками.

DRY. Пример -- реализация интерфейса ConsoleInterface, реализация списка команд через Enum и доступ к нему по методу commands() в Main.

Single Responsibility Principle. Пример -- интерфейсы и асбтрактные классы Category, Cart, Order и т.д., методы в имплементации интерфейса Shop. Все отвечают за свою область задач, связаны через интерфейс Shop.

Open/Close. Пример -- интерфейсы и абстрактные методы практически для всей фунциональности, protected и private поля у реализаций. Это же может служить и примером принципа Dependency inversion principle: интерфейс Shop и его имплементация за редким исключением ссылаются на интерфейсы.

Принцип Лисков явно не выражен: в принципе, я не стал наследовать Cart от List, хотя функциональность корзины близка к списку как таковому, но сама корзина -- не список, хотя и основана на нём.
