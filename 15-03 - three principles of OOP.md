# Три принципа ООП

На самом деле их четыре:
- Наследование
- Полиморфизм
- Инкапсуляция
- Абстракция

## Наследование

Под наследованием понимается возможность создания нового класса на базе существующего. Наследование предполагает наличие
отношения “является” между классом наследником и классом родителем. При этом класс потомок будет содержать те же 
атрибуты и методы, что и базовый (родитель) класс, но при этом его можно (и нужно) расширять через добавление новых 
методов и атрибутов.  
Примером базового класса, демонстрирующего наследование, можно определить класс “автомобиль”, имеющий атрибуты: масса, 
мощность двигателя, объем топливного бака и методы: завести и заглушить. У такого класса может быть потомок – “грузовой 
автомобиль”, он будет содержать те же атрибуты и методы, что и класс “автомобиль”, и дополнительные свойства: 
количество осей, мощность компрессора и т.д.

## Полиморфизм

Полиморфизм позволяет одинаково обращаться с объектами, имеющими однотипный интерфейс, независимо от внутренней 
реализации объекта. Другими словами этот принцип можно описать как - **ЕДИНЫЙ ИНТЕРФЕЙС, РАЗНАЯ РЕАЛИЗАЦИЯ**. 
Например. Все автомобили имеют схожий (однотипный) интерфейс управления: педали газа и тормоза, рулевое колесо, 
переключатель поворотов, выключатель света фар и т.д. Если науситься управлять одним автомобилем, например "Москвич", то
можно без особых проблем сесть за руль BMW, или за руль грузового авто, или автобуса.
С объектом класса "грузовой автомобиль” можно производить те же операции, что и с объектом класса “автомобиль”, т.к. 
первый является наследником второго, при этом обратное утверждение неверно (во всяком случае не всегда). Другими словами
полиморфизм предполагает разную реализацию методов с одинаковыми именами. Это очень полезно при наследовании, когда в 
классе наследнике можно переопределить методы класса родителя.

## Инкапсуляция

Под инкапсуляцией понимается объединение в рамках одной сущности (класса) определенных данных и методов для работы с 
ними (и не только). Например, можно определить класс “холодильник”, который будет содержать следующие данные: 
производитель, объем, количество камер хранения, потребляемая мощность и т.п., и методы: открыть/закрыть холодильник, 
включить/выключить, изменить температуру. При этом класс становится новым типом данных в рамках разрабатываемой 
программы. Можно создавать переменные этого нового типа, такие переменные называются объекты.  
Так же, инкапсуляция, подразумевает сокрытие внутреней реализации объекта, оставлюя доступной только открытый интерфейс
объекта.

## Абстракция

Абстракция – это процесс скрытия всего, кроме релевантной информации об объекте. Например, нам не нужно знать, как 
работают часы, чтобы использовать их для определения времени. Абстракция позволяет сосредоточиться на том, что делает 
объект, а не на том, как он это делает.  
Например, если рассмотреть самый первый телефон и сасый современный, то можно выделить несколько важных деталей для 
данных устройств: это способ набора номера и совершения вызова и способ приёма вызова. То как эти телефоны выполняют эти
действия пользователь не знает, да это и не особо важно для него. 