# Git — comandos que sempre esqueço

## Desfazer coisas
```bash
git restore arquivo.txt        # descarta mudanças não commitadas de um arquivo
git restore --staged arquivo   # tira do stage sem perder a mudança
git reset --soft HEAD~1        # desfaz o último commit, mantém as mudanças
```

## Branches
```bash
git switch -c minha-feature    # cria e entra no branch
git branch -d minha-feature    # apaga branch já mergeado
git push -u origin minha-feature
```

## Ver o que mudou
```bash
git log --oneline -10          # últimos 10 commits resumidos
git diff --staged              # o que vai entrar no próximo commit
```

## Dica
Commit pequeno e com mensagem no imperativo ("adiciona X", "corrige Y")
fica muito mais fácil de ler o histórico depois.
