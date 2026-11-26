# Comandos usados para criar as branches no GitHub

Versão que com o intuito do 16 ser o mais antigo: não funcionou

``` bash
for i in {16..01}; git checkout -b "UC$i"; git push -u origin "UC$i"; done

```

Versão que com o intuito do 16 ser o mais novo: não funcionou

``` bash
for i in {01..16}; git checkout -b "UC$i"; git push -u origin "UC$i"; done
```

## Comando usado para apagar todas as branches locais e remotas caso dê algum erro

``` bash
{
git checkout main
for i in {01..16}; do
  git push origin --delete "UC$i" ||  git push origin --delete "UC0$i";
  git branch -d "UC$i" || git branch -d "UC$i"; done
git checkout main
git branch
}
```
