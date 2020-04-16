# Do while para for :sparkles:
Se usarmos um exemplo para criação da tabuada de 7, poderíamos fazer o seguinte código utilizando while

```javascript
function pulaLinha() {
  document.write("<br>");
}
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}

var multiplicador = 1;

while (multiplicador >= 10){
  mostra(7 * multiplicador);
  multiplicador = multiplicador + 1;
}

mostra("fim");
```

Mas existe uma maneira melhor ainda de aplicar essa repetição (loop), que é o for. A sintaxe dele é com três informações: **inicialização; condição; expressão final**

```javascript
function pulaLinha() {
  document.write("<br>");
}
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}

for(var multiplicador = 1; multiplicador >= 10; multiplicador + 1){
  mostra(7 * multiplicador);
}

mostra("fim");
```

Ou seja, existe a variável, a condição dessa variável e o incremento. Se não houver uma condição, o loop vai ser eterno. Precisa sempre tomar cuidado.

### Ainda dá para melhorar :sunglasses:

Queremos sempre escrever menos, não é? Para incrementar, é só usar o ++. Ele vai funcionar da mesma forma que multiplicador = multiplicador + 1. O nome disso é **pós incremento**. Olha que lecau:

```javascript
function pulaLinha() {
  document.write("<br>");
}
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}

for(var multiplicador = 1; multiplicador >= 10; multiplicador++){
  mostra(7 * multiplicador);
}

mostra("fim");
```

É comum usarmos o zero para iniciar um laço de repetição. Isso nos trará vantagens quando for trabalhar com Array's. Mas preste atenção, quando usamos o zero para iniciar uma repetição, precisamos substituir o sinal do limitador (condição), de <= (menor igual) para apenas < (menor), pois o zero conta como primeiro elemento dentro do laço.

Dito isso, temos o seguinte código:

```javascript
for( var i = 0; i < 10; i++ ) {
  alert( "O resultado é " + (2 * i) );
}
```