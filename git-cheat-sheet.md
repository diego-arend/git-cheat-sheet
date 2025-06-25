### **Git Cheat Sheet**  
 
---

### **📦 Configuração Inicial**  
| Comando | Descrição |  
|---------|-----------|  
| `git config --global user.name "Seu Nome"` | Define seu nome no Git. |  
| `git config --global user.email "seu@email.com"` | Define seu e-mail no Git. |  

---

### **🌿 Branches (Ramificações)**  
| Comando | Descrição |  
|---------|-----------|  
| `git branch` | Lista **branches locais**. |  
| `git branch -a` | Lista **todas as branches (locais + remotas)**. |  
| `git branch -v` | Mostra branches com **último commit**. |  
| `git branch --merged` | Lista branches **já mescladas**. |  
| `git branch --no-merged` | Lista branches **não mescladas**. |  
| `git checkout -b nova-branch` | Cria **e muda** para uma nova branch. |  
| `git switch -c nova-branch` | Alternativa moderna para `checkout -b`. |  
| `git checkout main` | Muda para a branch `main`. |  
| `git switch main` | Versão moderna de `git checkout main`. |  
| `git branch -d branch-antiga` | **Deleta** uma branch local (se mesclada). |  
| `git branch -D branch-antiga` | **Força exclusão** (mesmo não mesclada). |  
| `git push origin --delete branch-remota` | Deleta uma branch **remota**. |  

---

### **🔄 Atualizando Branches**  
| Comando | Descrição |  
|---------|-----------|  
| `git fetch origin` | Busca alterações **sem modificar** seu código. |  
| `git pull origin main` | Puxa alterações e faz **merge**. |  
| `git pull --rebase origin main` | Puxa alterações e faz **rebase**. |  
| `git reset --hard origin/main` | **Sobrescreve** sua branch local com a remota. |  
| `git rebase --abort` | **Cancelar** rebase em andamento |

---

### **💾 Commits**  
| Comando | Descrição |  
|---------|-----------|  
| `git add .` | Adiciona **todos** os arquivos ao staging. |  
| `git add arquivo.txt` | Adiciona um **arquivo específico**. |  
| `git commit -m "Mensagem"` | Cria um commit com mensagem. |  
| `git commit --amend` | **Corrige** o último commit (local). |  
| `git reset --soft HEAD~1` | Remove o último commit (**mantém alterações**). |  
| `git reset --hard HEAD~1` | Remove o último commit (**perde alterações**). |  
| `git revert <hash>` | **Desfaz** um commit (cria novo commit). |  

---

### **🔍 Visualizando Alterações**  
| Comando | Descrição |  
|---------|-----------|  
| `git status` | Mostra **arquivos modificados/não rastreados**. |  
| `git diff` | Mostra **alterações não preparadas**. |  
| `git diff --staged` | Mostra **alterações preparadas**. |  
| `git log --oneline --graph` | Histórico de commits **resumido**. |  
| `git reflog` | Mostra **histórico completo** (incluindo `detached HEAD`). |  

---

### **🧹 Limpeza & Manutenção**  
| Comando | Descrição |  
|---------|-----------|  
| `git gc --prune=now` | **Limpa** objetos não referenciados. |  
| `git stash` | Guarda alterações **sem commit**. |  
| `git stash pop` | Recupera alterações **do stash**. |  

---

### **⚠️ Comandos Perigosos**  
| Comando | Descrição |  
|---------|-----------|  
| `git push --force` | **Sobrescreve** o histórico remoto. |  
| `git push --force-with-lease` | Versão mais segura de `--force`. |  
| `git reset --hard <hash>` | **Perde alterações** não commitadas. |  

---

### ** Git Submodules **  
| Comando | Descrição |  
|---------|-----------| 
| `git submodule add <URL_DO_REPOSITÓRIO> <CAMINHO_DESTINO>` | adiciona um submodulo ao projeto. | 
| `git submodule update --remote --merge` | **Sobrescreve** atualizar as referências dos submodules. |  
| `git submodule update --init --recursive` | inicializar os repositorios. |  
| `git submodule deinit --all` | Este comando irá **desinicializar** todos os submodules, **removendo** os conteúdos dos diretórios dos submodules (mas mantendo os diretórios vazios). |

---

### **📌 Dicas Rápidas**  
1. **Sempre confira `git status`** antes de commitar.  
2. **Prefira `rebase`** para branches locais e **`merge`** para branches compartilhadas.  
3. **Evite `--force`** em branches públicas.  
4. **Use mensagens claras** nos commits (ex: "Corrige bug no login").  

---

✨ **Pronto!** Agora você tem um guia completo dos comandos Git discutidos.  
Salve este cheat sheet e consulte quando precisar! 🚀