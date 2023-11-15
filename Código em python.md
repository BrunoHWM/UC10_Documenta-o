
### Código completo 
```
import pandas as pd

# Carregando o arquivo Excel
df = pd.read_excel("base_notas.xlsx")

# Calculando a média das notas e adicionando uma coluna 'Média'
df['Média'] = df[['Nota1', 'Nota2', 'Nota3', 'Nota4']].mean(axis=1)

# Salvando em um novo arquivo Excel
df.to_excel('nota_aluno.xlsx', index=False)

```

---

1. Esta linha importa a biblioteca Pandas e a renomeia como 'pd',
para encurtar o nome da biblioteca e facilitar o uso.
```
import pandas as pd
```

2. Este comando utiliza a função read_excel() do Pandas para ler um arquivo Excel chamado "base_notas.xlsx" e carregá-lo.
```
df = pd.read_excel("base_notas.xlsx")
```

3. Estamos calculando a média das notas de cada aluno. df[['Nota1', 'Nota2', 'Nota3', 'Nota4']] seleciona as colunas que contêm as notas individuais dos alunos. O método mean(axis=1) calcula a média ao longo do eixo das colunas (axis=1), ou seja, para cada linha. O resultado é armazenado na coluna 'Média'.
```
df['Média'] = df[['Nota1', 'Nota2', 'Nota3', 'Nota4']].mean(axis=1)
```

4. Este comando salva o DataFrame atualizado em um novo arquivo Excel chamado 'nota_aluno.xlsx'. O parâmetro index=False especifica que não queremos salvar o índice (números das linhas) do DataFrame no arquivo Excel, apenas os dados.
```
df.to_excel('nota_aluno.xlsx', index=False)
```
