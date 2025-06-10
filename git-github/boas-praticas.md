# Boas práticas de commits

Esse arquivo contém boas práticas para de commits. Utilização de **commits semânticos** para manter o histórico claro e organizado.

---

## Commits semânticos

Commits semânticos (Convention Commits) é uma maneira de formatar as mensagens dos commits de forma objetiva e clara.

- Usar commits semânticos traz mais clareza do histórico do projeto.
- Permite o versionamento semântico, geração automática de changelogs.
- Melhora a qualidade do código.
- Facilita a manutenção do código.

---

## 🧱 Estrutura básica

<tipo>: <mensagem curta e objetiva no imperativo>

---

### Tipos mais usados

| Tipo       | Descrição                                              | Exemplo                                             |
| ---------- | ------------------------------------------------------ | --------------------------------------------------- |
| `feat`     | Adiciona uma nova funcionalidade                       | feat: adiciona componete de login                   |
| `fix`      | Corrige um bug                                         | fix: corrige erro no botão de envio                 |
| `docs`     | Mudanças na documentação do projeto                    | docs: atualiza README com instruções de uso         |
| `style`    | Mudança de formatação (espaços, ponto e vírgula, etc.) | style: remove espaços extras no CSS                 |
| `refactor` | Refatoração de código (sem alterar comportamento)      | refactor: melhora legibilidade da função de cálculo |
| `test`     | Adição ou alteração de testes                          | test: adiciona teste para componete Header          |
| `chore`    | Tarefas que não afetam o código (ex: configs)          | chore: atualiza dependências do projeto             |

---

### Exemplos Convention Commits + Gitmoji

| Tipo     | Descrição                                         |
| -------- | ------------------------------------------------- |
| ✨ feat: | implementa sistema de cadastro de usuários        |
| 🐛 fix:  | corrige bug no formulário de login                |
| 📝 docs: | adiciona explicação sobre o fluxo de autenticação |

---

🔥 Emojis mais usados por Devs
🧱 Estrutura do Projeto / Sessões do README
Emoji Significado / Uso comum
📁 Pasta / diretório
📄 Arquivo
📝 Documentação / Notas
📌 Dicas / Informações importantes
🔖 Marcadores / Versões / Tags
📚 Recursos / Leitura
🧭 Navegação / Roadmap

🚀 Tecnologias / Ferramentas
Emoji Significado / Uso comum
💻 Código / Programação
🖥️ Front-end
🧠 Lógica / Algoritmos
🗄️ Back-end / Banco de Dados
⚙️ Configurações / Build
🧪 Testes
📦 Pacotes / Dependências
🧰 Ferramentas / DevTools

📌 Commits semânticos (prefixos com emojis)
Emoji Prefixo Significado
✨ feat: Nova funcionalidade
🐛 fix: Correção de bug
♻️ refactor: Refatoração de código
📚 docs: Alterações na documentação
🎨 style: Estilo (indentação, espaços, etc.)
✅ test: Adição/modificação de testes
🔥 perf: Melhorias de performance
🚀 chore: Tarefas de build, CI, configs, etc.

📈 Progresso / Status
Emoji Significado / Uso comum
🚧 Em construção / WIP (work in progress)
✅ Feito / Completo
🟡 Em andamento
❌ Cancelado / Removido
🆕 Novo
⏳ Aguardando

🤝 Contribuição / Comunidade
Emoji Significado / Uso comum
🙋‍♂️ Contribuidores
🧑‍💻 Desenvolvedores
🤝 Colaboração / Pull requests
💬 Discussões / Comentários

💡 Extras criativos
Emoji Significado / Uso comum
🎯 Objetivo / Meta
🧩 Parte de um todo / Módulo
🗺️ Roadmap / Planejamento
📊 Resultados / Métricas
🎉 Conquista / Primeira versão
⛏️ Trabalhando duro / Update

---

### 🔧 2. [Opcional] Instalar o **Commitizen** para te guiar nos commits

Commitizen te ajuda a escrever commits semânticos de forma interativa.

#### 📦 Como instalar:

```bash
npm install -g commitizen
```

#### 🚀 Como usar:

```bash
npx cz
```
