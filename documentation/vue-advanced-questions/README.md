# Vue Advanced
1. Существует ситуация когда нужно асинхронно из хранилища полуить данные и добавить в компонент если данных там еще нет
Данная ситуация приводит к тому что необхоимо выполнить такой код при иницилизации компонента
```javascript
created() {
    this.compoData = this.store.getters('someGetter')
}
```
и затем при добавлении данных в хранилище необходимо за ними проследить
```javascript
watch: {
    'store.getters' (newValue) {
          this.compoData = newValue
    }
}
```
:::answer
необходимо сделать ваш ватчер immediate true
```javascript
'store.getters': {
    heandler (newValue) {
      this.compoData = newValue
    }, 
    immediate: true
}
```
:::
2. Существует ситуация когда нужно при инициализации компонента к примеру подписать на событие DOM а перед тем когда компонент будет унечтожен отписаться от события
Это возмоэно сделать через доболнительную переменную коммпонента в которую можно сохранить подписку а затем делать отписку в нужный момент.
:::answer
 Более компактное решение:
```javascript
created() {
   const escapeHandler = e => {
      if (e.key === 'Escape' && this.show) {
        this.cancel()
      }
    }
    document.addEventListener('keydown', escapeHandler)
    this.$once('hook:destroyed', () => {
      document.removeEventListener('keydown', escapeHandler)
    })
}
```
:::
3. Как можно в асинхронном коде отображать Vue экземпляр, к примеру нужно проинецелизировать какие то данные которые приходять с сервера и затем только рендерить екземпляр Vue
:::answer
```javascript
var app = new Vue({
//modules
})
setTimeout(() => app.$mount('#app'), 1000)
```
:::
4. Что можно расказать об отрибуте `key` 
:::answer
Перемещает дом елементы
можно изменить ключь и можно <br>
перезапуск анимации
```html
<transition>
  <span :key="text">{{ text }}</span>
</transition>
```
перерендерить компонент
```html
<component :key="text"></component>
```
:::
5. Заем нужен аттрибут `key` в цикле `v-for` или в анимации `transition-group`
:::answer
Для того что бы отслеживать идентичность каждого элемента, что позволит переиспользовать и перемещать существующие элементы.
:::
6. Почему не будет работать анимация на функциональном компоненте используемом через тег `component` и как это исправит
:::answer
У функционального компоненте нет ключа при создании, ему нужно ключ повесить на root елемент
:::
7. Как обрабатывать события в функциоанальном компоненте и кастомные тоже
:::answer
```javascript
@before-hide="listeners['close']"
```
:::
8. Сбособы кастомизировить вид кнопки загрузки файла во `Vue`
```html
<input type="file" ref="fileLoader" style="display: none">
<button @click="$refs.fileLoader.click()">load file</button>
```
