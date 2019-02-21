# JS интевью
1. Как работает JS **(event loop)**
2. ООП и функциональное програмирование
3. Что такое асинхронная функция, что такое промисифицированая функция
4. Высплытие **(hoisting)** переменных и функций
5. Что такое ссылочные типы данных, базовые типы данных
6. Что такое **this**, поведение в функция. Отчличие стрелочных и обычных функций
7. Что такое **pure function**
8. Замыкание, лексическое окружение, карирование
9. **ES6** модули, какие приимущества (не попадает в глобальную область видимости)
10. Классы, паттерны проектирования, клыссы Set и Map
11. Методы сбособы итерации по массивам и объектам
12. Что такое и как работает **деструктуризация**
13. Как взять уникальные элементы из массива объектов, как сделать массив уникальных элементов
14. Рекурсия и древовидная структура 
15. Остаточные параметры и параметры по умалчанию в функциях
16. **Promise**, **async await**, **Promise.all() Promise.race()**
17. Всплытие браузерных событий по **DOM**
18. Класс **FileReader**, доступ к файловой системе
19. **try catch** блок
20. Класс **Proxy**, манипуляции с функциями
21. **WebSocket api** 
22. Регулярные выражения, методы
# JS интевью advanced 
1. **window** и **document**
2. Что такое атрибуты у ключа объекта
```javascript
Object.defineProperty(obj, 'key', {
    enumerable: false,
    configurable: false,
    writable: false,
    value: 'static'
    });
```
3. Где лучше хранить данные на стороне клиента (indexDB, local storage)
4. Как синхронизировать две вкладки, как слушать **localstorage** (на одно и тойже вкладке не будет слушать)
5. Какие события можно слушать на input, отличе **blur** и **focusout**(у первого нет дальнейшего всплытия) 
6. Какую анимацию и как использовать  **transition**, **animation**
7. Как отследить анимацию **transition**, **animation** (начало, окончание)
8. Тег `<pre>`, что он делает
9. Тег `<sript>`, **defer** (откладывает на конец загрузки документа) и  **async** (документ не ожидает загрузку скрипта) атрибуты 
10. Что такое **srcset**, **dataset** атрибуты на елементах
11. Как выровнять елемнт в контейнере по вертикали и горизонтали
12. Как открыть почтовый клиент `<a href="mailto:vlad@htmlbook.ru?subject=Вопрос по HTML">`
# Vue интевью
1. Как работает цикл компонента, где компонент не доступен, цикл **updated** и **nextTick** (updated не гарантирует что дочерние компоненты буду отрисованы)
2. Как работает реактивность, методы массива которые сохраняют реактивность, как исправить потерю реативности **Vue.$set()**, как сделать свойство не реактивным Object.freez()
3. Дерективы и фильтры, ползовательские дерективы (хуки **bind inserted update componentUpdated unbind**) и фильтры,
плагины **(Vue.use(plugin))** 
4. Props (type, default, required, validator), прокидывание данных обратно (какой способ предпочтительнее: cb, emmit)
5. Компоненты `<component>`, `<keep-alive>`+ 2 хука(activated, deactivated), `<transition>&<transition-group>` + хуки + аттрибуты 
6. Слоты, для чего нужны
7. Асинхронная  загрузка компонентов в роуте и локально в компоненте, дефолтные компоненты при асинхронной загрузке компонентов
8. Функциональные компоненты
9. $refs, $listeners, $attrs
10. События **@event** и модификаторы событий **.self . stop . once**
11. Если сделать computed свойство стрелочной функцией, что будет 
# Vuex интевью
1. Как брать данные из store, что такое кеширование геттеров
2. Как изменять состояние хранилища, ассинхронное митирование состояния (**rootState**, **rootGetters**)
3. Модули Vuex, как взять state из одного модуля в другом как менять состояние одного из другого `commit('module/mutation', data, {root:true})`
4. Плагины Vuex, подписка и отслеживаниеа мутаций
