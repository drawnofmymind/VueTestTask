# testtask

### Тестовое задание задание middle:

    1) Реализовать компоненты RadioGroup, RadioItem.
        RadioGroup должен группировать RadioItem и корректно 
        работать с пропсом disabled(должны становиться неактивными все вложенные RadioItem) 
        и c директивой v-model при изменении значений в RadioItem'ах. 
        Структура должна быть примерно следующей:

    <RadioGroup v-model="value" :disabled="disabled" />
        <RadioItem value="1">Значение 1<RadioItem />
        <RadioItem value="2">Значение 2<RadioItem />
        <RadioItem value="3">Значение 3<RadioItem />
    </RadioGroup>


    Способы взаимодействия компонентов RadioGroup и RadioItem может быть любым подходящим способом на ваш выбор кроме vuex

    RadioItem должен уметь работать как вложенным в RadioGroup, там и независимо сам и так же корректно взаимодействовать 
    с disabled и v-model.

    Важно: на странице может быть несколько RadioGroup и они должны группировать значения только в своей группе

    2) Необходимо реализовать компонент с методом validate.
       Компонент может быть вложен сам в себя.
       При вызове метода validate, необходимо что-бы компонент 
       вызвал данный метод у своих детей(только validate-items)
       Cхематчино:
       <validate-items>
            <some-component>
               <div>
                <validate-items> </validate-items>
                </div>
            </some-component>
            <some-component>
                <validate-items>
                    <validate-items />
                </validate-items>
            </some-component>
            <validate-component></validate-items>
       </validate-items>
    
    Вызов метода validate у компонента 1 должен вызвать данный метод у компонента 2,3,5.
    Вызов метода у компонента 3 должен вызвать метож у компонента 4.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### Customize configuration

                


