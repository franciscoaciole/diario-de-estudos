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

### Como nomear variáveis
- O nome deve descrever o que o dado representa
- Deve começar com letra, sublinhado (`_`) ou cifrão (`$`); **não** pode começar com número
- Diferencia maiúsculas de minúsculas: `age` e `Age` são variáveis diferentes
- Usar **camelCase**: primeira palavra minúscula, as seguintes com inicial maiúscula → `let thisIsCamelCase;`
- Palavras-chave (`let`, `const`, `function`, `return`) não podem ser nomes de variáveis
- Evitar caracteres especiais


## Aula 2 — let, const e var (18/11)

### let
- Declara variáveis que **podem ser reatribuídas** (recebem outro valor depois).
- Não pode ser **redeclarada** no mesmo escopo.
- Pense nela como um "contêiner flexível".

```js
let score = 10;
console.log(score); // 10
score = 20;
console.log(score); // 20
```

### const
- Declara variáveis que **não podem ser reatribuídas**.
- Precisa receber um valor **na hora da declaração**, senão dá erro.
- É ideal para valores que não devem mudar por acidente.
- Se guardar uma lista ou um objeto, o **conteúdo** ainda pode mudar. Só a variável não aponta para outro valor.

```js
const maxScore = 100;
console.log(maxScore); // 100
maxScore = 200; // erro: não pode reatribuir
```

### var
- É a forma antiga de declarar variáveis e **não é recomendada**.
- Funciona parecido com `let`, mas tem **escopo amplo** (vaza para fora dos blocos `{ }`), o que aumenta a chance de bugs.

### Resumo
| Palavra | Reatribuir? | Redeclarar? | Usar? |
|---------|-------------|-------------|-------|
| `let`   | Sim         | Não         | Sim   |
| `const` | Não         | Não         | Sim (padrão) |
| `var`   | Sim         | Sim         | Evitar |

> **Dica:** use `const` por padrão e troque para `let` só quando o valor precisar mudar.
