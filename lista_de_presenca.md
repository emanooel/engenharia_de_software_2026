# Engenharia de Software 2026
## Lista de presença
* Emanoel

Entendido. Como a classe já está instanciada no `main.py`, o foco deles será puramente a **interação com o objeto** e o **fluxo de trabalho do Git**. 

Seguindo sua preferência por sinceridade e detalhamento, aqui está uma proposta de enunciado técnica e direta, ideal para estudantes de Engenharia de Software no IFES:

---

## 🚀 Exercício: Colaboração e Padronização com Git (Pull Request)

O objetivo desta tarefa é simular um ambiente real de desenvolvimento, onde múltiplos desenvolvedores contribuem para um mesmo repositório seguindo padrões de nomenclatura e fluxo de trabalho.

### 1. Sincronização e Branching
Antes de qualquer alteração, você deve garantir que sua base está atualizada e criar uma ramificação isolada. **Nunca trabalhe diretamente na branch `main`.**

* **Padrão de Branch:** `feature/presenca-[seu-nome-sobrenome]` (em minúsculas, sem espaços ou acentos).
* **Comandos:**
    ```bash
    git checkout main
    git pull origin main
    git checkout -b feature/presenca-joao-silva
    ```

### 2. Implementação do Código
No arquivo `main.py`, localize o objeto já instanciado da classe `Alunos`. Sua única tarefa é chamar o método `inserir` passando o seu nome como argumento.

* **Exemplo de código esperado:**
    ```python
    # O objeto 'lista_turma' (ou o nome definido no arquivo) já existe.
    lista_turma.inserir("João Silva")
    ```

### 3. O "Commit" Semântico
A mensagem de commit é a documentação histórica do projeto. Utilizaremos o padrão **Conventional Commits**. Como estamos adicionando uma funcionalidade/dado, o prefixo será `feat`.

* **Padrão:** `feat: adiciona [Seu Nome] à lista de presença`
* **Comandos:**
    ```bash
    git add main.py
    git commit -m "feat: adiciona Joao Silva à lista de presença"
    ```

### 4. Push e Pull Request (PR)
Envie sua branch para o repositório remoto e abra um **Pull Request** para a branch `main`.

* **Comando:**
    ```bash
    git push origin feature/presenca-joao-silva
    ```
* **No GitHub/GitLab:** No campo de descrição do PR, informe que você concluiu a inserção do seu nome para o registro de presença da aula de Engenharia de Software.

---

### ⚠️ Regras de Ouro (Sinceridade Técnica)

Para que seu PR seja aceito, os seguintes pontos serão avaliados:

1.  **Higiene do Git:** Se a branch estiver fora do padrão ou o commit for genérico (ex: "ajuste", "teste", "v1"), o PR será rejeitado.
2.  **Conflitos:** Se outro aluno editou a mesma linha, você precisará resolver o conflito localmente antes de eu fazer o merge.
3.  **Sintaxe:** Certifique-se de que não quebrou a indentação do arquivo `main.py`.

---

### Tabela de Referência Rápida

| Ação | Padrão / Exemplo |
| :--- | :--- |
| **Branch** | `feature/presenca-emanoel-martins` |
| **Tipo de Commit** | `feat:` (para novas entradas/funções) |
| **Mensagem** | `feat: adiciona [Nome] à lista de alunos` |

---

**Posso te ajudar a configurar alguma regra de proteção de branch no seu repositório para impedir que eles deem push direto na `main` sem passar pelo PR?**