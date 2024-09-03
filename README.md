# Estrutura do diretório para Exercícios Não-Exame

Este documento descreve a estrutura de diretórios e arquivos necessária para organizar exercícios não-exame. Por favor, siga esta estrutura ao organizar e enviar os exercícios.

## Estrutura de Diretórios

A estrutura de diretórios para cada exercício deve seguir o padrão abaixo:

<aside>

/diretório_base/<nome_disciplina>/<ano_escolaridade>º_ano/<nome_tópico>/<nome_subtópico>/<identificador_exercício>/

</aside>

### Descrição dos Elementos:

- **diretório_base/**: Diretório principal onde todos os exercícios são armazenados.
- **<nome_disciplina>/**: Nome da disciplina a que o exercício pertence (por exemplo, "Matemática_A", "Português").
- **<ano_escolaridade>_ano/**: Ano de escolaridade em que o exercício é aplicado (por exemplo, "10_ano").
- **<nome_tópico>/**: Nome do tópico abrangido pelo exercício (por exemplo, "Álgebra", "Óptica").
- **<nome_subtópico>/**: Nome do subtópico específico dentro do tópico (por exemplo, "Equações Lineares", "Refração").
- **<identificador_exercício>/**: Identificador único do exercício, que pode ser um código ou descrição curta.

## Conteúdo da Pasta do Exercício

Dentro da pasta `<identificador_exercício>/`, devem estar os seguintes ficheiros:

1. **question.<extensão>**
    - O ficheiro que contém o enunciado do exercício.
    - Formatos suportados: `.png`, `.jpg`, `.jpeg`, `.pdf`.
    - Exemplo: `question.pdf`.
2. **tip<número>. <extensão>**
    - Ficheiros que contêm explicações ou dicas para resolver o exercício.
    - Formatos suportados: `.png`, `.jpg`, `.jpeg`, `.pdf`.
    - O número (`<número>`) indica a sequência das dicas (por exemplo, `tip1.pdf`, `tip2.jpg`).
    - Exemplo: `tip1.png`.
3. **info.json**
    - Um ficheiro JSON que contém metadados importantes sobre o exercício.
    - Exemplo de estrutura do ficheiro `info.json`:

```json
{
	"answer": "A",
	"difficulty": 1
}

```

### Descrição dos Elementos no `info.json`:

- **answer**:
    - Indique a letra correspondente à resposta correta, caso o exercício seja de múltipla escolha.
    - Se o exercício não for de múltipla escolha, deixe este campo vazio (`""`).
- **difficulty**:
    - Um valor inteiro que representa a dificuldade do exercício:
        - `1`: Fácil
        - `2`: Médio
        - `3`: Difícil

## Exemplo de Estrutura

Aqui está um exemplo de como a estrutura de diretórios pode ser organizada:

```bash
/diretório_base/Matemática_A/10_ano/Álgebra/Equações_Lineares/123/
│   ├── question.png
│   ├── tip1.png
│   ├── tip2.png
│   ├── info.json
```

Neste exemplo, o exercício está relacionado com "Matemática A", destinado ao "10º ano", dentro do tópico "Álgebra" e subtópico "Equações Lineares". O identificador do exercício é apenas o número "123".

## Observações Finais

- Certifique-se de que todos os ficheiros estão devidamente nomeados e colocados na pasta correta.
- Revise o ficheiro `info.json` para garantir que as informações estão precisas.
