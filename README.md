# code-challenge-III

## Problema: Question Bank Manager

Você está desenvolvendo um sistema para gerenciar um banco de questões para professores. Cada questão possui os atributos:

- **id** (string ou número identificador)
- **disciplina** (string, ex: 'Matemática', 'História')
- **dificuldade** (inteiro, de 1 a 10)
- **enunciado** (string, texto da questão)
- **tags** (array de strings)

O objetivo é filtrar e retornar as questões que atendam a certos critérios, por exemplo, de uma disciplina específica e com dificuldade mínima.

### Entrada

- Uma lista de objetos, cada representando uma questão com os atributos: `id`, `disciplina`, `dificuldade`, `enunciado` e `tags`.
- Dois parâmetros de filtro: `disciplinaFiltro` (string) e `dificuldadeMinima` (inteiro).

### Saída

- Uma lista das questões que pertencem à disciplina especificada, que tenham dificuldade maior ou igual à dificuldade mínima e com no mínimo uma tag.

### Regras e Restrições

1. **Processamento em Blocos:**
   - O algoritmo deve processar as questões em blocos de tamanho 5, simulando cenários com grandes conjuntos de dados.
2. **Tempo Máximo de Execução:**
   - A solução deve ser executada em menos de 100ms para uma lista de 100 questões. Utilize `console.time()` e `console.timeEnd()` para medir o tempo de execução.
3. **Limite de Complexidade:**
   - Garanta que sua solução não exceda uma complexidade de O(n log n).

### Exemplo

```javascript
const questions = [
  {
    id: 1,
    disciplina: "Matemática",
    dificuldade: 8,
    enunciado: "Qual o valor de π?",
    tags: ["geometria"],
  },
  {
    id: 2,
    disciplina: "História",
    dificuldade: 5,
    enunciado: "Quem foi Napoleão?",
    tags: ["guerras"],
  },
  {
    id: 3,
    disciplina: "Matemática",
    dificuldade: 6,
    enunciado: "Resolver equações do 2º grau",
    tags: ["algebra"],
  },
  {
    id: 4,
    disciplina: "Matemática",
    dificuldade: 9,
    enunciado: "Cálculo integral",
    tags: ["calculo"],
  },
  {
    id: 5,
    disciplina: "Ciências",
    dificuldade: 7,
    enunciado: "Explicar o efeito estufa",
    tags: ["geografia"],
  },
];

const disciplinaFiltro = 'matematica';
const dificuldadeMinima = 7;

function filtrarQuestoes(questoes, disciplinaFiltro, dificuldadeMinima) {
  // Sua solução aqui
  // Lembre-se de processar as questões em blocos de 5
}

console.time('execucao');
console.log(filtrarQuestoes(questoes, disciplinaFiltro, dificuldadeMinima));
console.timeEnd('execucao');

// Saída esperada: array contendo, por exemplo, as questões com id 1 e 4.
```

```javascript
// array com 100 questoes para teste final de performance
const questoes = [
  {
    "id":1,
    "disciplina":"Matemática",
    "dificuldade":8,
    "enunciado":"Qual o valor de π?",
    "tags":[
      "geometria"
    ]
  },
  {
    "id":2,
    "disciplina":"História",
    "dificuldade":5,
    "enunciado":"Quem foi Napoleão?",
    "tags":[
      "guerras"
    ]
  },
  {
    "id":3,
    "disciplina":"Matemática",
    "dificuldade":6,
    "enunciado":"Resolver equações do 2º grau",
    "tags":[
      "algebra"
    ]
  },
  {
    "id":4,
    "disciplina":"Matemática",
    "dificuldade":9,
    "enunciado":"Cálculo integral",
    "tags":[
      "calculo"
    ]
  },
  {
    "id":5,
    "disciplina":"Ciências",
    "dificuldade":7,
    "enunciado":"Explicar o efeito estufa",
    "tags":[
      "geografia"
    ]
  },
  {
    "id":6,
    "disciplina":"Filosofia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 6 de Filosofia",
    "tags":[
      "epistemologia"
    ]
  },
  {
    "id":7,
    "disciplina":"Ciências",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 7 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":8,
    "disciplina":"Inglês",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 8 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":9,
    "disciplina":"Inglês",
    "dificuldade":6,
    "enunciado":"Enunciado da questão 9 de Inglês",
    "tags":[
      "vocabulario"
    ]
  },
  {
    "id":10,
    "disciplina":"Inglês",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 10 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":11,
    "disciplina":"Sociologia",
    "dificuldade":6,
    "enunciado":"Enunciado da questão 11 de Sociologia",
    "tags":[
      "cultura"
    ]
  },
  {
    "id":12,
    "disciplina":"História",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 12 de História",
    "tags":[
      "guerras"
    ]
  },
  {
    "id":13,
    "disciplina":"Filosofia",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 13 de Filosofia",
    "tags":[
      "epistemologia"
    ]
  },
  {
    "id":14,
    "disciplina":"Ciências",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 14 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":15,
    "disciplina":"Sociologia",
    "dificuldade":6,
    "enunciado":"Enunciado da questão 15 de Sociologia",
    "tags":[
      "cultura"
    ]
  },
  {
    "id":16,
    "disciplina":"Português",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 16 de Português",
    "tags":[
      "ortografia"
    ]
  },
  {
    "id":17,
    "disciplina":"Filosofia",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 17 de Filosofia",
    "tags":[
      "epistemologia"
    ]
  },
  {
    "id":18,
    "disciplina":"Português",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 18 de Português",
    "tags":[
      "interpretação"
    ]
  },
  {
    "id":19,
    "disciplina":"Geografia",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 19 de Geografia",
    "tags":[
      "vegetação"
    ]
  },
  {
    "id":20,
    "disciplina":"Geografia",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 20 de Geografia",
    "tags":[
      "relevo"
    ]
  },
  {
    "id":21,
    "disciplina":"Ciências",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 21 de Ciências",
    "tags":[
      "astronomia"
    ]
  },
  {
    "id":22,
    "disciplina":"Inglês",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 22 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":23,
    "disciplina":"Geografia",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 23 de Geografia",
    "tags":[
      "cartografia"
    ]
  },
  {
    "id":24,
    "disciplina":"Inglês",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 24 de Inglês",
    "tags":[
      "tradução"
    ]
  },
  {
    "id":25,
    "disciplina":"Português",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 25 de Português",
    "tags":[
      "ortografia"
    ]
  },
  {
    "id":26,
    "disciplina":"Ciências",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 26 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":27,
    "disciplina":"Filosofia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 27 de Filosofia",
    "tags":[
      "existencialismo"
    ]
  },
  {
    "id":28,
    "disciplina":"Geografia",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 28 de Geografia",
    "tags":[
      "vegetação"
    ]
  },
  {
    "id":29,
    "disciplina":"Sociologia",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 29 de Sociologia",
    "tags":[
      "sociedade"
    ]
  },
  {
    "id":30,
    "disciplina":"Matemática",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 30 de Matemática",
    "tags":[
      "geometria"
    ]
  },
  {
    "id":31,
    "disciplina":"Inglês",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 31 de Inglês",
    "tags":[
      "vocabulario"
    ]
  },
  {
    "id":32,
    "disciplina":"Sociologia",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 32 de Sociologia",
    "tags":[
      "sociedade"
    ]
  },
  {
    "id":33,
    "disciplina":"Inglês",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 33 de Inglês",
    "tags":[
      "tradução"
    ]
  },
  {
    "id":34,
    "disciplina":"Filosofia",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 34 de Filosofia",
    "tags":[
      "existencialismo"
    ]
  },
  {
    "id":35,
    "disciplina":"Geografia",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 35 de Geografia",
    "tags":[
      "relevo"
    ]
  },
  {
    "id":36,
    "disciplina":"Ciências",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 36 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":37,
    "disciplina":"Geografia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 37 de Geografia",
    "tags":[
      "clima"
    ]
  },
  {
    "id":38,
    "disciplina":"História",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 38 de História",
    "tags":[
      "brasil"
    ]
  },
  {
    "id":39,
    "disciplina":"Inglês",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 39 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":40,
    "disciplina":"Ciências",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 40 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":41,
    "disciplina":"Português",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 41 de Português",
    "tags":[
      "literatura"
    ]
  },
  {
    "id":42,
    "disciplina":"Inglês",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 42 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":43,
    "disciplina":"Português",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 43 de Português",
    "tags":[
      "gramatica"
    ]
  },
  {
    "id":44,
    "disciplina":"Português",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 44 de Português",
    "tags":[
      "ortografia"
    ]
  },
  {
    "id":45,
    "disciplina":"Matemática",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 45 de Matemática",
    "tags":[
      "geometria"
    ]
  },
  {
    "id":46,
    "disciplina":"Ciências",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 46 de Ciências",
    "tags":[
      "astronomia"
    ]
  },
  {
    "id":47,
    "disciplina":"Filosofia",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 47 de Filosofia",
    "tags":[
      "lógica"
    ]
  },
  {
    "id":48,
    "disciplina":"Ciências",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 48 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":49,
    "disciplina":"Ciências",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 49 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":50,
    "disciplina":"Português",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 50 de Português",
    "tags":[
      "interpretação"
    ]
  },
  {
    "id":51,
    "disciplina":"Português",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 51 de Português",
    "tags":[
      "literatura"
    ]
  },
  {
    "id":52,
    "disciplina":"História",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 52 de História",
    "tags":[
      "guerras"
    ]
  },
  {
    "id":53,
    "disciplina":"Inglês",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 53 de Inglês",
    "tags":[
      "tradução"
    ]
  },
  {
    "id":54,
    "disciplina":"Inglês",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 54 de Inglês",
    "tags":[
      "verbos"
    ]
  },
  {
    "id":55,
    "disciplina":"História",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 55 de História",
    "tags":[
      "guerras"
    ]
  },
  {
    "id":56,
    "disciplina":"Ciências",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 56 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":57,
    "disciplina":"Filosofia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 57 de Filosofia",
    "tags":[
      "existencialismo"
    ]
  },
  {
    "id":58,
    "disciplina":"Filosofia",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 58 de Filosofia",
    "tags":[
      "existencialismo"
    ]
  },
  {
    "id":59,
    "disciplina":"História",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 59 de História",
    "tags":[
      "brasil"
    ]
  },
  {
    "id":60,
    "disciplina":"Geografia",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 60 de Geografia",
    "tags":[
      "clima"
    ]
  },
  {
    "id":61,
    "disciplina":"Matemática",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 61 de Matemática",
    "tags":[
      "probabilidade"
    ]
  },
  {
    "id":62,
    "disciplina":"Sociologia",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 62 de Sociologia",
    "tags":[
      "trabalho"
    ]
  },
  {
    "id":63,
    "disciplina":"Português",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 63 de Português",
    "tags":[
      "gramatica"
    ]
  },
  {
    "id":64,
    "disciplina":"Filosofia",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 64 de Filosofia",
    "tags":[
      "lógica"
    ]
  },
  {
    "id":65,
    "disciplina":"Português",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 65 de Português",
    "tags":[
      "literatura"
    ]
  },
  {
    "id":66,
    "disciplina":"Inglês",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 66 de Inglês",
    "tags":[
      "tradução"
    ]
  },
  {
    "id":67,
    "disciplina":"Matemática",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 67 de Matemática",
    "tags":[
      "algebra"
    ]
  },
  {
    "id":68,
    "disciplina":"Filosofia",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 68 de Filosofia",
    "tags":[
      "lógica"
    ]
  },
  {
    "id":69,
    "disciplina":"Geografia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 69 de Geografia",
    "tags":[
      "hidrografia"
    ]
  },
  {
    "id":70,
    "disciplina":"História",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 70 de História",
    "tags":[
      "brasil"
    ]
  },
  {
    "id":71,
    "disciplina":"Matemática",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 71 de Matemática",
    "tags":[
      "estatistica"
    ]
  },
  {
    "id":72,
    "disciplina":"Português",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 72 de Português",
    "tags":[
      "ortografia"
    ]
  },
  {
    "id":73,
    "disciplina":"Sociologia",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 73 de Sociologia",
    "tags":[
      "trabalho"
    ]
  },
  {
    "id":74,
    "disciplina":"Matemática",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 74 de Matemática",
    "tags":[
      "geometria"
    ]
  },
  {
    "id":75,
    "disciplina":"História",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 75 de História",
    "tags":[
      "revoluções"
    ]
  },
  {
    "id":76,
    "disciplina":"História",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 76 de História",
    "tags":[
      "idade moderna"
    ]
  },
  {
    "id":77,
    "disciplina":"Português",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 77 de Português",
    "tags":[
      "gramatica"
    ]
  },
  {
    "id":78,
    "disciplina":"História",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 78 de História",
    "tags":[
      "guerras"
    ]
  },
  {
    "id":79,
    "disciplina":"Inglês",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 79 de Inglês",
    "tags":[
      "tradução"
    ]
  },
  {
    "id":80,
    "disciplina":"Matemática",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 80 de Matemática",
    "tags":[
      "probabilidade"
    ]
  },
  {
    "id":81,
    "disciplina":"Português",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 81 de Português",
    "tags":[
      "literatura"
    ]
  },
  {
    "id":82,
    "disciplina":"Filosofia",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 82 de Filosofia",
    "tags":[
      "filosofia antiga"
    ]
  },
  {
    "id":83,
    "disciplina":"Filosofia",
    "dificuldade":1,
    "enunciado":"Enunciado da questão 83 de Filosofia",
    "tags":[
      "filosofia antiga"
    ]
  },
  {
    "id":84,
    "disciplina":"História",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 84 de História",
    "tags":[
      "revoluções"
    ]
  },
  {
    "id":85,
    "disciplina":"Português",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 85 de Português",
    "tags":[
      "redação"
    ]
  },
  {
    "id":86,
    "disciplina":"Sociologia",
    "dificuldade":10,
    "enunciado":"Enunciado da questão 86 de Sociologia",
    "tags":[
      "trabalho"
    ]
  },
  {
    "id":87,
    "disciplina":"Sociologia",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 87 de Sociologia",
    "tags":[
      "trabalho"
    ]
  },
  {
    "id":88,
    "disciplina":"Ciências",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 88 de Ciências",
    "tags":[
      "biologia"
    ]
  },
  {
    "id":89,
    "disciplina":"Filosofia",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 89 de Filosofia",
    "tags":[
      "epistemologia"
    ]
  },
  {
    "id":90,
    "disciplina":"História",
    "dificuldade":2,
    "enunciado":"Enunciado da questão 90 de História",
    "tags":[
      "brasil"
    ]
  },
  {
    "id":91,
    "disciplina":"Filosofia",
    "dificuldade":8,
    "enunciado":"Enunciado da questão 91 de Filosofia",
    "tags":[
      "filosofia antiga"
    ]
  },
  {
    "id":92,
    "disciplina":"História",
    "dificuldade":6,
    "enunciado":"Enunciado da questão 92 de História",
    "tags":[
      "brasil"
    ]
  },
  {
    "id":93,
    "disciplina":"Português",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 93 de Português",
    "tags":[
      "interpretação"
    ]
  },
  {
    "id":94,
    "disciplina":"História",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 94 de História",
    "tags":[
      "idade media"
    ]
  },
  {
    "id":95,
    "disciplina":"Inglês",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 95 de Inglês",
    "tags":[
      "gramatica"
    ]
  },
  {
    "id":96,
    "disciplina":"Filosofia",
    "dificuldade":5,
    "enunciado":"Enunciado da questão 96 de Filosofia",
    "tags":[
      "ética"
    ]
  },
  {
    "id":97,
    "disciplina":"Inglês",
    "dificuldade":7,
    "enunciado":"Enunciado da questão 97 de Inglês",
    "tags":[
      "leitura"
    ]
  },
  {
    "id":98,
    "disciplina":"Matemática",
    "dificuldade":3,
    "enunciado":"Enunciado da questão 98 de Matemática",
    "tags":[
      "geometria"
    ]
  },
  {
    "id":99,
    "disciplina":"Ciências",
    "dificuldade":9,
    "enunciado":"Enunciado da questão 99 de Ciências",
    "tags":[
      "quimica"
    ]
  },
  {
    "id":100,
    "disciplina":"Filosofia",
    "dificuldade":4,
    "enunciado":"Enunciado da questão 100 de Filosofia",
    "tags":[
      "epistemologia"
    ]
  }
];
```
