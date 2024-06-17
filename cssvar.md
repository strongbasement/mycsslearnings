# css variables
1. proper way to define css varible
```css
:root{
    --color-text:blue;
}
```
2. we can also use a fallback value for variables
```css

h1
{
    color:var(--color-text,green);
}


```

3. you can overwrite variables

```css
:root{
    --color-text:blue;
}
.card
{
     --color-text:orange;
}

```

4. the above feature will be very usefull in responsive designs and preferred color scheme


```css
@media (prefers-color-scheme:dark){
    :root
    {
        --color:white;

    }
}


```

5. you can also use css variables like this

```css

:root{
    --red:45;
    --blue:84;
    --green:45;

}

h1{
    color:rgb(var(--red),var(--blue),var(--green));
}
```
6.A mini project to manipute css elemments property by js


*things to know:
  *event listners
  *js code to set style property

```js

//code to manipulate style proprty for root
document.documentElement.style.setProperty('--color','blue');


//manipulate individual elements

const element =document.getElementById('sdiv');
element.style.setProperty('--color','blue');


```