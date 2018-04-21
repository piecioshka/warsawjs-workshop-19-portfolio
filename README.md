# warsawjs-workshop-19-portfolio 

> Aplikacja stworzona na potrzeby WarsawJS Workshop #19

![](http://warsawjs.com/assets/images/logo/logo-transparent-240x240.png)

---

## ✨ Demo ✨

https://piecioshka.github.io/warsawjs-workshop-19-portfolio/app/

## :rocket: Deployment :rocket:

### GitHub Pages

1. Wejdź do `Settings`
2. Przeskroluj do sekcji `GitHub Pages`
3. `Source` wybierz brancha `master`
    - pojawi się link do strony

Link nie wyświetla Twojego projektu?
- spr. czy dopisałeś `app/` do linku
- spr. czy masz plik `index.html` w katalogu `app`
- dodaj plik `.nojekyll` do katalogu głównego projektu

## :bulb: O czym opowiedzieć? :bulb:

Slajdy dostępne pod tym adresem: https://github.com/piecioshka/slides-warsawjs-workshop-19-front-end-beginner

## Zakres funkcjonalności projektu

> Typ projektu: landing page

- [x] Baner
    - https://picsum.photos/720/300
- [x] Galeria zdjęć
    - https://picsum.photos/300/300
- [x] Newsletter
- [x] Menu
    - [x] Skrolowanie do sekcji za pomocą hashtaga
- [ ] Karuzela: Podgląd powiększonych zdjęć

## Krok po kroku

### Etap 0. Beforek :beer:

0. Stworzyć workspace-u
0. Stworzyć katalogu projektu
0. Stworzyć katalogu `app`
0. Stworzyć plik `app/index.html`
0. W pliku `index.html` wpisujemy podstawowe tagi:
    html, head, body
0. Wykorzystać tagi title, meta

### Etap 1: Baner

0. W `body` dodać kontener `div` o id `page`
0. Wewnątrz tagu `div` dodać `section` o id `banner` (język angielski)
0. Dodać nagłówek pierwszego poziomu `h1` z tekstem `Portfolio`
0. Stworzyć plik `app/styles/main.css`
0. Osadzić plik CSS w HTMLu za pomocą `<link rel="stylesheet" href="styles/main.css"/>`
0. Zresetować domyślne style (reguła `margin`) dla przeglądarki dla `body, h1, p`
0. Zdefiniować szerokość strony na `720px` za pomocą reguły `width`
0. Wycentrować kontener `#page` definiując automatyczne marginesy `margin-left` i `margin-right`
0. Zdefiniować wysokość dla kontenera `.banner`
0. Ustawić tło za pomocą reguły `background-image`
0. Wyłączyć powtarzanie
0. Wycentrować tło
0. Wycentrować text w banerze za pomocą `Flexbox`

    ```css
    .banner {
        // ...
        display: flex;
        justify-content: center;
        align-items: center;
    }
    ```

### Etap 2: Galeria zdjęć

0. Stworzyć kontener `section` o id `gallery` z nagłówkiem `h1` o treści `Galeria zdjęć`
0. Stworzyć listę za pomocą tagów `ul, li`
0. Każdy element list powinien zawierać obrazek (wykorzystać tą samą usługę
    zdjęć co w banerze)

    UWAGA: Obrazek osadzamy za pomocą znacznika `img`

0. Zresetować domyślne style dla list ul, li

    ```css
    ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }
    ```

0. Zmienić sposób prezentacji zdjęć w galerii za pomocą Flexboxa

    ```css
    ul {
        // ...
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    ```

### Etap 3: Newsletter (Wykorzystujemy `JavaScript`)

0. Stworzyć kontener `section` o id `newsletter` z nagłówkiem `h1` o treści `Newsletter`
0. Dodać pod nagłówkiem formularz za pomocą znacznika `form`
0. Stworzyć `input` typu `email` z atrybutem `name` o treści `email`
0. Dodatkowe: Ustawić atrybut `required`
0. Stworzyć `label` z zawartością Twój email
0. Stworzyć `input` typu `submit` z atrybutem `value` o treści `Wyślij`
0. Stworzyć plik `app/scripts/main.js`
0. Osadzić plik JavaScript w HTMLu za pomocą `<script src="scripts/main.js"></script>`
    
    UWAGA: osadzić ten kod przed zamknięciem znacznika `body`
    
0. Stworzyć w pliku JavaScript zmienną, która będzie przechowywała referencję do formularza
0. Podpiąć się pod zdarzenia `submit` na formularzu
0. Wyłączyć domyślne zachowanie formularza w ciele handlera zdarzenia `submit` za pomocą funkcji `evt.preventDefault()`
0. Stworzyć wewnątrz handler zmienną przechowującą dane wpisane w formularzu

    Wykorzystać do tego `FormData`

0. Skonwertować dane z formularza na mapę za pomocą konstruktora `Map`
0. Stworzyć funkcję `displayMessage` do prezentacji komunikatu, który zostanie
    przekazany w pierwszym parametrze
0. Zbudować wiadomość z wykorzystaniem `template stringów` i stworzyć zmienną `message`
0. Przekazać zmienną `message` podczas uruchomienia funkcji `displayMessage`

### Etap 4: Menu

0. Stworzyć kontener `nav` o id `menu`
0. Stworzyć listę za pomocą `ul, li` wewnątrz nowo stworzonego kontenera
0. Stworzyć link w każdym elemencie listy
    
    UWAGA: wykorzystujemy znacznik `a`

0. Zdefiniować odpowiedni wartości w atrybucie `href` aby po hashtagu były
    wartości z `id` każdej sekcji
0. (Opcjonalne) Ostylować elementy menu według uznania

### Etap 4: Karuzela (Wykorzystujemy `JavaScript`)

Dla chętnych 🏆

## Źródła, czyli tam gdzie warto zajrzeć

- https://github.com/piecioshka/colors - kolory
- https://picsum.photos/ - darmowe zdjęcia
- https://flexboxfroggy.com/ - nauka Flexboxa
- https://experiments.withgoogle.com/chrome
- https://codepen.io/joshnh/pen/paxbE
- https://codepen.io/piecioshka/pens/loved/10/
- https://codepen.io/eva_trostlos/pen/akQoLN
- https://codepen.io/aakashrodrigues/pen/Gfhjw

## License

[The MIT License](http://piecioshka.mit-license.org) @ 2018
