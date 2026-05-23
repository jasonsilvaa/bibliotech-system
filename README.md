# BiblioTech - Sistema de Gestão de Biblioteca Escolar

O **BiblioTech** é uma solução dedicada à gestão eficiente de acervos em bibliotecas escolares, focada em facilitar a busca de títulos e a reserva de exemplares para alunos e gestores.

## 🚀 Sobre o Projeto
Este projeto foi desenvolvido com foco em boas práticas de engenharia de software e garantia de qualidade (QA). O objetivo é modernizar o fluxo de acesso a livros em ambientes académicos, garantindo uma interface intuitiva e processos de busca robustos.

## 📋 Funcionalidades Principais
- **Busca Avançada:** Pesquisa por título ou nome do autor.
- **Sistema de Reservas:** Reserva imediata de livros disponíveis.
- **Validação de Filtros:** Filtro de ano de publicação com tratamento de erros (1900–2026).
- **Interface Segura:** Bloqueio de inputs inválidos e mensagens de erro amigáveis.

## 🛠️ Stack Tecnológica & Práticas
- **Metodologia:** BDD (Behavior Driven Development).
- **Documentação:** Gherkin para cenários de teste.
- **QA:** Testes exploratórios documentados e rastreabilidade de requisitos.

## 📝 Documentação Técnica
Para mais detalhes, consulte os documentos disponíveis na pasta `/docs`:
* [Mapa de Requisitos e Matriz de Rastreabilidade](docs/DOCUMENTACAO.md)
* [Sprint Simulada: Práticas BDD](docs/Sprint_Simulada.md)
* [Relatórios de Testes Exploratórios](docs/Relatorio_Teste_Exploratorio.md)

---
## 🧪 Exemplo de Cenário (Gherkin)
```gherkin
Dado que o aluno está na página inicial de busca do sistema;
Quando o aluno deixa o campo de busca em branco;
E clica no botão "Buscar";
Então o sistema deve exibir a mensagem de erro: "Por favor, preencha o campo título".
✒️ Autor
[Jason Silva/[GitHub](https://github.com/jasonsilvaa)]

Projeto desenvolvido para fins de demonstração de práticas de Engenharia de Software e Qualidade (QA).
