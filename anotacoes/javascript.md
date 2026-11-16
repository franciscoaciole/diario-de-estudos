# Anotações — JavaScript (freeCodeCamp)

## 16/11/2026

### Comentários
```js
// comentário de uma linha
/* comentário de
   várias linhas */
```

### Tipos de dados
- **Number** = números inteiros e decimais (ponto flutuante: 3.14, 7.2)
- **String** = usada para representar nomes, rótulos, mensagens...
- **Boolean** = true ou false
- **undefined** = variável declarada sem valor
- **null** = variável definida como "nada" intencionalmente; não contém nenhum valor
- **Object** = coleção de pares chave-valor
- **Symbol** = tipo especial de valor, sempre único e imutável; usado para criar identificadores únicos para propriedades
- **BigInt** = usado para números grandes que excedem o Number

> Symbol e BigInt são menos comuns, porém é interessante saber.

### Variáveis
- São caixas que armazenam valores, para consultar sempre que preciso
- `let age;` → declara a variável
- `=` → **operador de atribuição** (coloca um valor na variável): `let age = 20;`
- Vantagem do `let`: permite reatribuir valores

### Regras de nomes
- O nome deve descrever o que o dado representa
- Deve começar com letra, sublinhado (`_`) ou cifrão (`$`); **não** pode começar com número
- Diferencia maiúsculas de minúsculas: `age` e `Age` são variáveis diferentes
- Usar **camelCase**: primeira palavra minúscula, as seguintes com inicial maiúscula → `let thisIsCamelCase;`
- Palavras-chave (`let`, `const`, `function`, `return`) não podem ser nomes de variáveis
- Evitar caracteres especiais
