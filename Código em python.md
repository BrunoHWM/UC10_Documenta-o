
### Código completo 
```
import pandas as pd

# Carregando o arquivo Excel
df = pd.read_excel("base_notas.xlsx")

# Calculando a média das notas e adicionando uma coluna 'Média'
df['Média'] = df[['Nota1', 'Nota2', 'Nota3', 'Nota4']].mean(axis=1)

# Salvando o DataFrame atualizado em um novo arquivo Excel
df.to_excel('nota_aluno.xlsx', index=False)

```

---

1. Esta linha importa a biblioteca Pandas e a renomeia como 'pd',
para encurtar o nome da biblioteca e facilitar o uso.
```
import pandas as pd
```
