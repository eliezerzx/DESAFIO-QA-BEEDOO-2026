# Relatório de Bugs

Este documento registra os problemas encontrados durante a execução dos testes no módulo de cadastro e listagem de cursos da aplicação.

## BUG 01 - Curso não é removido da lista após exclusão

Curso não é removido da lista após clicar em "Excluir curso"

**Severidade:** Alta

**Passos para reproduzir:**

1 - Acessar a aplicação

2 - Cadastrar um novo curso preenchendo todos os campos

3 - Ir para a tela "Listar cursos"

4 - Clicar no botão "Excluir curso"

5 - Observar o comportamento da aplicação

**Resultado atual:**
O sistema exibe a mensagem "Curso excluído com sucesso!", porém o curso continua aparecendo na lista de cursos.

**Resultado esperado:**
Após clicar em "Excluir curso", o curso deveria ser removido da lista imediatamente.

**Evidência:**
Ver imagem na pasta `/evidencias/bug_exclusao.png`

## BUG 02 - Permite cadastro com Data de Fim anterior à Data de Início

**Descrição:**  
O sistema aceita o cadastro de cursos onde a data de encerramento ocorre antes da data de início.

**Severidade:** Alta (Erro de Lógica de Negócio)

**Passos para reproduzir:**

1 - Acessar a aba **"Cadastrar Curso"**.

2 - Preencher o campo **"Data de Início"** com uma data futura (ex: 20/04/2026).

3 - Preencher o campo **"Data de Fim"** com uma data passada (ex: 10/03/2025).

4 - Preencher os demais campos.

5 - Clicar em **"Cadastrar Curso"**.

**Resultado atual:**  
O curso é cadastrado com sucesso e exibido na listagem com cronologia invertida.

**Resultado esperado:**  
O sistema deve validar as datas e impedir o cadastro, exibindo um alerta como:  
*"A data de término não pode ser anterior à data de início".*

**Evidência:**  
Ver imagens na pasta `/evidencias`:
- `cadastro_invalido.png`
- `cadastro_invalido2.png`

---

## BUG 03 - Ausência de validação de URL no campo de imagem

**Descrição:**  
O sistema aceita textos comuns no campo de **URL da imagem de capa**, resultando em erro visual na listagem.

**Severidade:** Média (Interface/UI)

**Passos para reproduzir:**
1 - Acessar a aba **"Cadastrar Curso"**.
2 - No campo **"URL da imagem de capa"**, digitar apenas `teste` ou qualquer texto que não seja um link válido.
3 - Finalizar o cadastro do curso.
4 - Ir para a tela **"Listar cursos"**.

**Resultado atual:**  
O curso é listado, porém o card exibe uma **imagem quebrada ou espaço vazio**, pois o link informado é inválido.

**Resultado esperado:**  
O sistema deve validar se o texto inserido é uma **URL válida**, por exemplo iniciando com:
- `http://`
- `https://`

**Evidência:**  
Ver imagem na pasta `/evidencias`:
- `cadastro_invalido2.png`

---

## BUG 04 - Permite cadastro de curso com 0 vagas

**Descrição:**  
O sistema permite a criação de um curso sem vagas disponíveis.

**Severidade:** Média (Regra de Negócio)

**Passos para reproduzir:**
1 - Acessar a aba **"Cadastrar Curso"**.
2 - No campo **"Número de vagas"**, inserir o valor `0`.
3 - Clicar em **"Cadastrar Curso"**.

**Resultado atual:**  
O sistema permite o cadastro e exibe **"0 vagas"** na listagem principal.

**Resultado esperado:**  
O sistema deveria exigir **no mínimo 1 vaga**, ou exibir uma mensagem informando que o curso não possui vagas disponíveis.

**Evidência:**  
Ver imagem na pasta `/evidencias`:
- `cadastro_invalido.png`
