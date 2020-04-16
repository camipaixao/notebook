# Sobre for e while
Se usarmos um exemplo para criação de uma tabuada, poderíamos fazer o seguinte código utilizando while

```javascript
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}
var multiplicador = 1;
while (multiplicador >= 10){
  mostra(7 * multiplicador);
  multiplicador = multiplicado + 1;
}
mostra("fim :)");
```