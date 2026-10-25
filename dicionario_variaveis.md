# Dicionário de Variáveis – Base de Dados Simulada (Frota Movida 2025)

**Companhia Auditada:** Movida Participações S.A. (B3: MOVI3)
**Matrícula do Preparador:** 232029597
**Conta Contábil Objeto:** Ativo Imobilizado Consolidado – Subconta Veículos (Nota Explicativa 12 das DFs de 2025)
**Natureza dos Dados:** Dados Sintéticos / Simulados para fins estritamente didáticos (conforme item 3 do roteiro da prova)
**Quantidade de Registos:** 500.000 linhas
**Ficheiro de Referência:** `base_simulada_frota_movida_2025.csv`

## 1. Estrutura das Variáveis (Colunas da Base)

| Nome da Variável (Coluna) | Tipo de Dado | Formato / Unidade | Descrição Técnica e Regra de Negócio |
| :--- | :--- | :--- | :--- |
| **`CHASSI_ID`** | Texto (*String*) | Alfanumérico (17 caracteres) | Código alfanumérico individual simulado representativo do chassi do veículo (chave primária do registo analítico). |
| **`PLACA`** | Texto (*String*) | Alfanumérico (`MOV0000`) | Identificação simulada de matrícula/emplacamento do veículo na frota. |
| **`SEGMENTO`** | Texto (*String*) | Categórico (`RAC` ou `GTF`) | Linha de negócio da Movida à qual o veículo está alocado (RAC - *Rent a Car* ou GTF - Gestão e Terceirização de Frotas). |
| **`MODELO`** | Texto (*String*) | Texto livre | Descrição da marca, modelo e versão de motorização do veículo adquirido das montadoras. |
| **`DATA_AQUISICAO`** | Data (*Date*) | `AAAA-MM-DD` | Data contabilística de aquisição e entrada em operação do veículo no ativo imobilizado. |
| **`VALOR_CUSTO`** | Numérico (*Float*) | Reais (R$) com 2 casas decimais | Custo histórico de aquisição original faturado do bem junto à montadora. |
| **`DEPRECIACAO_ACUM`** | Numérico (*Float*) | Reais (R$) com 2 casas decimais | Montante acumulado da depreciação linear até 31/12/2025. |
| **`VALOR_LIQUIDO`** | Numérico (*Float*) | Reais (R$) com 2 casas decimais | Valor contabilístico líquido do veículo em 31/12/2025 (`VALOR_CUSTO - DEPRECIACAO_ACUM`), conciliado com a Nota 12. |

## 2. Conciliação com as Demonstrações Contabilísticas (DFP 2025) e Exceções Inseridas

Conforme exigido no item 3 das instruções, a base foi parametrizada para conciliar com o saldo contabilístico líquido da Nota Explicativa 12:
* **Saldo Contabilístico Oficial (Nota 12 – Veículos Líquido em 31/12/2025):** R$ 22.972.473.000,00 (R$ 22.972.473 mil).
* **Saldo da Base Simulada Antes da Injeção de Erros:** R$ 22.972.473.000,00 (Conciliação exata: diferença de R$ 0,00).
* **Saldo da Base Simulada Após Injeção de Erros para Testes (PT 530):** R$ 22.970.609.858,28.
* **Diferença Líquida Conciliada (Efeito das Exceções Simuladas):** -R$ 1.863.141,72 (decorrente exclusivamente da substituição de 40 itens por saldos negativos).

### Registo de Erros/Inconsistências Sintéticas Inseridas (Gabarito de Teste PT 530):
1. **Exceção de Valorização (`ERR-01`):** 40 registos tiveram o seu `VALOR_LIQUIDO` alterado para `-2500.00` para teste de filtro lógico de valorização.
2. **Exceção de Corte Temporal / *Cut-off* (`ERR-02`):** 30 registos tiveram a sua `DATA_AQUISICAO` alterada para `2026-02-20` para teste de validação temporal (> 31/12/2025).
3. **Exceção de Existência / Duplicidade (`ERR-03`):** 25 registos tiveram o seu `CHASSI_ID` igualado ao código do primeiro item (`9BGMOV25000000001`) para teste de chave primária duplicada.
