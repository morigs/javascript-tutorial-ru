Есть два основных подхода.

1. Можно хранить сами цены в "копейках" (центах и т.п.). Тогда они всегда будут целые и проблема исчезнет. Но при показе и при обмене данными нужно будет это учитывать и не забывать делить на 100.
2. При операциях, когда необходимо получить окончательный результат -- округлять до 2-го знака после запятой. Все, что дальше -- ошибка округления:

    ```js run no-beautify
    var price1 = 0.1, price2 = 0.2;
    alert( +(price1 + price2).toFixed(2) );
    ```
