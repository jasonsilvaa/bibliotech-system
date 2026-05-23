# Documentação Técnica: Sistema BiblioTech

## 1. Mapa de Requisitos
O Mapa de Requisitos consolida as necessidades de negócio identificadas, categorizando-as em especificações funcionais e não funcionais[cite: 2].

| ID | Categoria | Descrição do Requisito | Prioridade |
|:---|:---|:---|:---|
| **RF-01** | Funcional | O sistema deve permitir que o aluno realize a busca de livros no acervo através do título ou do nome do autor. | Alta |
| **RF-02** | Funcional | O sistema deve permitir que o aluno realize a reserva imediata de um livro se este constar como disponível. | Alta |
| **RNF-01** | Não Funcional | O sistema deve suportar até 500 acessos simultâneos sem degradação do serviço. | Alta |

---

## 2. Matriz de Rastreabilidade de Requisitos (MRR)
A Matriz garante a cobertura total entre o pedido de negócio e a validação técnica[cite: 2].

| ID | Origem | Módulo / Tela | Caso de Teste | Status |
|:---|:---|:---|:---|:---|
| **RF-01** | Diretora | Tela de Busca | CT-01, CT-02, CT-03, CT-04 | Em Dev |
| **RF-02** | Diretora | Módulo de Reserva | CT-05: Reserva de livro | Em Revisão |

---

## 3. Plano de Testes

### 3.1 Escopo e Objetivos
* **No Escopo:** Validação de mecanismos de pesquisa (filtros) e fluxo de reserva de itens[cite: 2].
* **Fora do Escopo:** Testes de carga/stress (RNF-01)[cite: 2].

### 3.2 Estratégia
* **Testes Funcionais:** Validação das queries de pesquisa e estados de reserva[cite: 2].
* **Testes de Usabilidade:** Garantia de interface intuitiva para o corpo discente[cite: 2].

### 3.3 Ambientes
* **Ciclo:** QA (Interno) -> Pré-produção (Staging)[cite: 2].
* **Plataforma:** Google Chrome[cite: 2].
* **Hardware:** Terminais físicos da biblioteca escolar[cite: 2].

### 3.4 Critérios de Aceitação
* Busca deve retornar correspondências exatas[cite: 2].
* **Contingência:** Em caso de falha crítica na "Reserva", autoriza-se o deploy parcial (apenas módulo de Busca)[cite: 2].

---

## 4. Caderno de Casos de Teste Manuais

### [CT-01] — Buscar livro existente por título E autor
* **Pré-condições:** Usuário na 'Tela de Busca'; Livro 'Dom Casmurro' cadastrado[cite: 2].
* **Passo-a-passo:**
    1. Digitar 'Dom Casmurro' no campo Título.
    2. Digitar 'Machado de Assis' no campo Autor.
    3. Clicar em 'Buscar'.
* **Resultado Esperado:** O sistema exibe o card do livro 'Dom Casmurro'[cite: 2].

### [CT-02] — Buscar livro inexistente
* **Pré-condições:** Usuário na 'Tela de Busca'; Livro 'O Senhor dos Anéis' NÃO cadastrado[cite: 2].
* **Passo-a-passo:**
    1. Digitar 'O Senhor dos Anéis' no campo Título.
    2. Clicar em 'Buscar'.
* **Resultado Esperado:** Exibir a mensagem: 'O livro não está disponível no momento'[cite: 2].

### [CT-03] — Buscar livro APENAS por título
* **Pré-condições:** Usuário na 'Tela de Busca'; Livro 'Dom Casmurro' cadastrado[cite: 2].
* **Passo-a-passo:**
    1. Digitar 'Dom Casmurro' no campo Título.
    2. Deixar campo Autor em branco.
    3. Clicar em 'Buscar'.
* **Resultado Esperado:** O sistema traz o livro pesquisado em uma lista[cite: 2].

### [CT-04] — Buscar livros APENAS por autor
* **Pré-condições:** Usuário na 'Tela de Busca'; Livros do autor 'Machado de Assis' cadastrados[cite: 2].
* **Passo-a-passo:**
    1. Deixar campo Título em branco.
    2. Digitar 'Machado de Assis' no campo Autor.
    3. Clicar em 'Buscar'.
* **Resultado Esperado:** O sistema traz todos os livros cadastrados daquele autor em uma lista[cite: 2].
