# Sobre for e while
Se usarmos um exemplo para criação da tabuada de 7, poderíamos fazer o seguinte código utilizando while

```javascript
function pulaLinha() {
  document.write("<br>");
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

mostra("fim :)");
```

Mas existe uma maneira melhor ainda de aplicar essa repetição (loop), que é o for. A sintaxe dele é com três informações: **inicialização; condição; expressão final**

```javascript
function pulaLinha() {
  document.write("<br>");
  document.write("<br>");
}
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}

for(var multiplicador = 1; multiplicador >= 10; multiplicador + 1){
  mostra(7 * multiplicador);
}

mostra("fim :)");
```

Ou seja, existe a variável, a condição dessa variável e o incremento. Se não houver uma condição, o loop vai ser eterno. Precisa sempre tomar cuidado.

### Ainda dá para melhorar :sparkles:

Queremos sempre escrever menos, não é? Para incrementar, é só usar o ++. Ele vai funcionar da mesma forma que multiplicador = multiplicador + 1. O nome disso é **pós incremento**. Olha que lecau:

```javascript
function pulaLinha() {
  document.write("<br>");
  document.write("<br>");
}
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}

for(var multiplicador = 1; multiplicador >= 10; multiplicador++){
  mostra(7 * multiplicador);
}

mostra("fim :)");
```