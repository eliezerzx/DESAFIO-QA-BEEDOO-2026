# DESAFIO-QA-BEEDOO-2026

## 📌 Sobre o desafio

Este repositório contém a análise e os testes realizados no módulo de **cadastro e listagem de cursos** da aplicação disponibilizada para o desafio técnico de QA.

A aplicação testada está disponível no link abaixo:

https://creative-sherbet-a51eac.netlify.app/

O objetivo deste desafio é demonstrar habilidades de **análise de sistema, criação de cenários de teste, execução de testes e registro de bugs**, além de apresentar clareza na documentação e organização das evidências.

---

# 🔎 Análise inicial da aplicação

A aplicação tem como objetivo permitir o **cadastro e a visualização de cursos**.

O sistema possibilita que o usuário preencha um formulário contendo informações do curso, como:

* Nome do curso
* Descrição
* Instrutor
* URL da imagem de capa
* Link de inscrição
* Data de início
* Data de fim
* Número de vagas
* Tipo de curso (Online ou Presencial)

Após o cadastro, os cursos ficam disponíveis em uma **lista**, onde é possível visualizar as informações cadastradas e realizar a **exclusão do curso**.

A aplicação aparenta simular um sistema simples de **gestão de cursos**.

---

# 🔄 Principais fluxos da aplicação

Durante a exploração da aplicação foram identificados os seguintes fluxos principais:

## 1. Cadastro de curso

1. Acessar a aba **Cadastrar Curso**
2. Preencher os campos do formulário
3. Clicar no botão **Cadastrar Curso**
4. O curso é adicionado ao sistema
5. O curso aparece na listagem de cursos

---

## 2. Listagem de cursos

1. Acessar a aba **Listar Cursos**
2. Visualizar os cursos cadastrados
3. Ver informações como:

   * Nome
   * Instrutor
   * Datas
   * Número de vagas
   * Tipo de curso

---

## 3. Exclusão de curso

1. Acessar a lista de cursos
2. Clicar no botão **Excluir curso**
3. O sistema deve remover o curso da listagem

---

# ⚠️ Pontos críticos para teste

Durante a análise da aplicação foram identificados alguns pontos que exigem maior atenção nos testes:

* Validação dos campos obrigatórios no cadastro
* Validação das datas (data de início e data de fim)
* Validação de URLs (imagem e link de inscrição)
* Validação do número de vagas
* Persistência dos dados após cadastro
* Funcionamento correto da exclusão de cursos
* Comportamento da interface em cenários de erro
* Exibição correta dos cursos na listagem

---

# 🧠 Decisões tomadas para criação dos testes

Os cenários de teste foram elaborados considerando:

* Fluxo principal da aplicação (cadastro de curso)
* Exibição correta dos cursos cadastrados
* Testes de validação de campos
* Cenários negativos
* Possíveis comportamentos inesperados

Os testes foram priorizados com foco em **regras de negócio e validações de entrada de dados**, pois essas áreas geralmente apresentam maior risco de falhas.

---

# 🧪 Cenários e casos de teste

Os cenários e casos de teste foram documentados em uma planilha no Google Sheets.

A planilha contém:

* ID do caso de teste
* Cenário
* Passos para execução
* Resultado esperado
* Resultado obtido
* Status do teste
* Evidências

Acesse a planilha no link abaixo:

**[PLANILHA GOOGLE SHEETS](https://docs.google.com/spreadsheets/d/1PUgbj_Kmz_ygddUCnLfPJrI9pRmUHJnqLWEogOQSQsA/edit?usp=sharing)**

## Documentação Complementar

A documentação detalhada da análise e estratégia de testes pode ser acessada no link abaixo:

(https://docs.google.com/document/d/1KBcxB-Jn1RjmkWpOPQ6iAASHfk7DNu1xUtf5nsLNovM/edit?usp=sharing)

---

# 🐞 Registro de bugs

Durante a execução dos testes foram identificados alguns comportamentos inesperados na aplicação.

Os bugs encontrados foram documentados no arquivo:

📄 **bugs.md**

Entre os problemas identificados estão:

* Falha na exclusão de cursos
* Falta de validação de datas
* Falta de validação de URLs
* Permissão de cadastro de curso com 0 vagas

Cada bug contém:

* Título
* Passos para reprodução
* Resultado atual
* Resultado esperado
* Severidade
* Evidências

---

# 📷 Evidências dos testes

As evidências da execução dos testes foram registradas por meio de **prints de tela**.

Elas podem ser encontradas na pasta:

📁 **/evidencias**

Os arquivos incluem capturas como:

* Cadastro de cursos
* Listagem de cursos
* Execução de cenários de teste
* Demonstração dos bugs encontrados

---

# 🤖 Uso de Inteligência Artificial

Ferramentas de Inteligência Artificial foram utilizadas como **apoio durante a criação do cadastro do curso com ideias como "Introdução ao Python" e organização das informações**.

A IA foi utilizada apenas como **ferramenta de suporte**, mantendo sempre o raciocínio analítico durante a execução do desafio.

---

# 📁 Estrutura do repositório

```
DESAFIO-QA-BEEDOO-2026
│
├── README.md
├── bugs.md
├── evidencias/
│   ├── cadastro.png
│   ├── cadastro_invalido.png
│   ├── cadastro_invalido2.png
│   └── bug_exclusao.png
```

---

# ✅ Conclusão

A partir da análise exploratória e da execução dos testes foi possível identificar algumas falhas relacionadas principalmente a **validação de dados e lógica de negócio**.

Os testes realizados buscaram cobrir os fluxos principais da aplicação e também cenários negativos que podem impactar diretamente a experiência do usuário.

A documentação apresentada neste repositório demonstra o processo de análise, criação de testes, execução e registro de defeitos encontrados durante o desafio.
