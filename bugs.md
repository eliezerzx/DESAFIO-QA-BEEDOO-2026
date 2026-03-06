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
