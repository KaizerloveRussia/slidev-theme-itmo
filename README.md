# Тема ITMO для Slidev
Скачивание темы из регистра npm и последующая установка выполняется командой `npm install slidev-theme-itmo`. 

Для использования темы в `headmatter` презентации добавляется запись `theme: itmo` (slidev-theme- можно опустить), а для каждого слайда в соответствие с макетом презентации ИТМО аналогичной записью указывается используемый `layout`, доступны следующие:


1) **Cover** (не имеет именованных слотов);

2) **SecondCover** (не имеет именованных слотов);

3) **ThreeTextFields** (::header::, ::field1::, ::field2::, ::field3::);

4) **TextFieldRight** (::header::, ::field1::);

5) **OnlyText** (::header::, ::field1::);

6) **ThreeIllustrations** (::header::, ::boldText-1::, ::regularText-1::, ::boldText-2::, ::regularText-2::, ::boldText-3::, ::regularText-3::).

***
Наполнение слайдов осуществляется путем заполнения указанных слотов в `.md` разметке презентации, например:

```
# 1 слайд
---
layout: Cover
---
# Разметка Cover не имеет именованных слотов, так что просто указываем заголовок ниже пунктирной черты.
Slide Title


# 2 слайд
---
layout: SecondCover
---
Second Title


# Перескочим на 3 слайд
---
layout: ThreeTextFields
---

::header::
Slide Title

::field1::
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


::field2::
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```
