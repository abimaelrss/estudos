# Comandos básicos de Git

Esse arquivo contém um resumo dos principais comandos básicos de Git.

---

## Comandos repositório local

| Comando | Finalidade |
| --- | --- |
| `git init` | Inicia um repositório Git |
| `git status` | Verifica o estado atual do repositório |
| `git add .` | Adiciona todos os arquivos e alterações no diretório atual ao staging (preparando-os para o commit) |
| `git add <nome-do-arquivo>` | Adiciona alterações de um arquivo específico ao staging |
| `git rm --cached` | Remove alterações adicionadas ao staging |
| `git restore <nome-do-arquivo>` | Restaura arquivos e desfaz alterações locais |
| `git commit -m "mensagem"` | Registra alterações no repositório com uma mensagem descrevendo o que foi modificado |
| `git log` | Exibe histórico de commits |
| `git checkout <id-do-commit>` | Volta a versões anteriores de commits - Cria/Troca de branch |

---

## Comandos repositório remoto

| Comando | Finalidade |
| --- | --- |
| `git pull` | Atualiza local com o repositório remoto |
| `git push` | Envia alterações para o GitHub |
| `git clone` | Cria uma cópia local de um repositório remoto |

---