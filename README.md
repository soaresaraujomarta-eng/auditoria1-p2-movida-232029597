# Dossiê de Auditoria Independente (Didático) — Movida Participações S.A. (2025)

* **Universidade de Brasília (UnB)** — Departamento de Ciências Contábeis e Atuariais (CCA)
* **Disciplina:** CCA0024 - Auditoria 1 (Turma 02 - 2026.2)
* **Professor:** Lucas Oliveira Gomes Ferreira
* **Matrícula do Preparador:** 232029597
* **Companhia Atribuída:** Movida Participações S.A. (B3: MOVI3 | CNPJ: 21.314.559/0001-66)
* **Exercício Auditado:** Encerrado em 31 de dezembro de 2025 (com comparativos de 2024)

---

## 1. Download da Base de Dados Simulada (500.000 linhas)
Conforme item 6 das instruções da avaliação, como o arquivo CSV contendo os 500.000 registros analíticos da frota (Ativo Imobilizado - Subconta Veículos) ultrapassa o limite de 25 MB da interface web do GitHub, a base completa está disponível para download imediato no link abaixo:

* 🔗 **Link para Download da Base Simulada (`base_simulada_frota_movida_2025.csv`):** [https://drive.google.com/file/d/1CEEnEh5iE7_GNUy1FkxLBE7Igr4Boj-y/view?usp=drive_link]

---

## 2. Organização do Repositório
* `Dossie_Auditoria_Movida_2025.pdf`: Dossiê completo contendo os 24 Papéis de Trabalho (PT EC e PT 200 a PT 600) e os Programas de Auditoria por ciclo operacional, com referências cruzadas.
* `dicionario_variaveis.md`: Dicionário técnico detalhando as variáveis da base simulada, premissas de geração, conciliação contábil e registro das exceções inseridas.
* `gerar_base_movida.py` / `.ipynb`: Código-fonte em Python utilizado para geração reprodutível das 500.000 linhas e testes substantivos/amostragem (PT 530).
* `amostra_selecionada_pt530.xlsx`: Planilha editável contendo a amostra extraída e os cálculos de suporte.

---

## 3. Instruções para Reprodução do Trabalho
1. Certifique-se de possuir o Python 3.10+ instalado com as bibliotecas `pandas`, `numpy` e `openpyxl` (ou utilize o ambiente Google Colab).
2. Execute o script `gerar_base_movida.py`. Como a semente aleatória foi fixada na matrícula (`np.random.seed(232029597)`), o script gerará exatamente os mesmos 500.000 registros conciliados com o saldo de R$ 22.972.473 mil da Nota Explicativa 12 das DFs de 2025 e injetará as mesmas 95 exceções sintéticas de controle.
3. Em seguida, execute o bloco de auditoria e amostragem para reproduzir a conciliação, a detecção via CAAT (população integral) e a extração da amostra estatística de 384 itens (`amostra_selecionada_pt530.xlsx`).

---

## 4. Matriz de Cobertura das Normas (NBC TA Vigentes em 2025)

| Papel de Trabalho | Norma NBC TA | Versão / Vigência Consultada (CFC) | Status / Localização |
| :--- | :--- | :--- | :--- |
| **PT EC** | NBC TA Estrutura Conceitual | Resolução CFC nº 1.202/09 (Alt. NBC TA EC 2015) | Concluído no Dossiê PDF |
| **PT 200** | NBC TA 200 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 210** | NBC TA 210 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 220** | NBC TA 220 (R3) | Vigente a partir de 15/12/2022 | Concluído no Dossiê PDF |
| **PT 230** | NBC TA 230 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 240** | NBC TA 240 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 250** | NBC TA 250 (R1) | Vigente a partir de 15/12/2017 | Concluído no Dossiê PDF |
| **PT 260** | NBC TA 260 (R2) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 265** | NBC TA 265 | Resolução CFC nº 1.210/09 | Concluído no Dossiê PDF |
| **PT 300** | NBC TA 300 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 315** | NBC TA 315 (R2) | Vigente a partir de 15/12/2021 | Concluído no Dossiê PDF |
| **PT 320** | NBC TA 320 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 330** | NBC TA 330 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 402** | NBC TA 402 | Resolução CFC nº 1.215/09 | Concluído no Dossiê PDF |
| **PT 450** | NBC TA 450 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 500** | NBC TA 500 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 501** | NBC TA 501 | Resolução CFC nº 1.218/09 | Concluído no Dossiê PDF |
| **PT 505** | NBC TA 505 | Resolução CFC nº 1.219/09 | Concluído no Dossiê PDF |
| **PT 510** | NBC TA 510 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 520** | NBC TA 520 | Resolução CFC nº 1.221/09 | Concluído no Dossiê PDF |
| **PT 530** | NBC TA 530 | Resolução CFC nº 1.222/09 | Concluído no Dossiê PDF |
| **PT 540** | NBC TA 540 (R2) | Vigente a partir de 01/01/2020 | Concluído no Dossiê PDF |
| **PT 550** | NBC TA 550 | Resolução CFC nº 1.224/09 | Concluído no Dossiê PDF |
| **PT 560** | NBC TA 560 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 570** | NBC TA 570 | Vigente a partir de 31/12/2016 | Concluído no Dossiê PDF |
| **PT 580** | NBC TA 580 (R1) | Vigente a partir de 01/01/2017 | Concluído no Dossiê PDF |
| **PT 600** | NBC TA 600 (R2) | Vigente a partir de 15/12/2023 | Concluído no Dossiê PDF |

---

## 5. Relação de Fontes Públicas Utilizadas

1. **Demonstrações Financeiras Padronizadas (DFP) Anuais Completas 2025 — Movida Participações S.A.**
   * **Documento:** Relatório da Administração, Balanço Patrimonial, DRE, DRA, DMPL, DFC, DVA, Notas Explicativas (1 a 30), Relatório do Auditor Independente (PwC) e Relatório do CAE (137 páginas).
   * **Exercício correspondente:** Findo em 31/12/2025 (comparativo 31/12/2024).
   * **Endereço eletrônico (RI Movida / CVM):** https://ri.movida.com.br/ e https://www.gov.br/cvm/
   * **Data de acesso:** 25/10/2026.
   * **Páginas utilizadas:** Páginas 1 a 137 (Numeração interna DFs: págs. 1 a 104; DFP CVM: págs. 1 a 27).
2. **Conselho Federal de Contabilidade (CFC) — Normas Brasileiras de Contabilidade (NBC TA)**
   * **Endereço eletrônico:** https://cfc.org.br/tecnica/normas-brasileiras-de-contabilidade/nbc-ta-de-auditoria-independente/
   * **Data de acesso:** 25/10/2026.

---

## 6. Conclusão Integrada do Trabalho (Item 6 do Edital)

Com base nos exames documentais realizados sobre as Demonstrações Financeiras de 2025 da **Movida Participações S.A.** e nos procedimentos simulados executados para fins estritamente acadêmicos, conclui-se de forma integrada que:
1. **Riscos Identificados:** Os riscos significativos da companhia concentram-se na **mensuração do valor residual e vida útil econômica da frota de veículos** (Ativo Imobilizado líquido de R$ 24,16 bilhões, representando 69,18% do Ativo Total), na **contabilização e valor justo de instrumentos financeiros derivativos e *hedge accounting*** (passivo de derivativos de R$ 734,8 milhões e reclassificação de R$ 839,1 milhões de hedge de fluxo de caixa para valor justo), na **gestão da liquidez e cumprimento de *covenants* financeiros** frente ao capital circulante líquido negativo de R$ 5,63 bilhões no consolidado, e no intenso volume de **transações com partes relacionadas do Grupo SIMPAR** (R$ 522,6 milhões em vendas de ativos).
2. **Procedimentos Realizados e Evidências:** Foram executados procedimentos analíticos reais (PT 520), conciliações documentais (PT 500), avaliação de estimativas (PT 540), revisão de eventos subsequentes até março de 2026 (PT 560) e testes substantivos informatizados e por amostragem estatística sobre a base simulada de 500.000 registros da frota (PT 530). As distorções sintéticas intencionalmente injetadas na base simulada (totalizando R$ 4,94 milhões de impacto bruto) ficaram substancialmente abaixo da Materialidade de Execução (R$ 131,04 milhões), demonstrando a eficácia dos testes desenhados.
3. **Limitações do Trabalho e Declaração de Não Emissão de Opinião:** O presente dossiê possui natureza exclusivamente didática. Procedimentos que dependem de acesso físico, sistemas internos (ERP SAP), leitura de atas privadas ou circularizações externas reais foram apenas planejados ou simulados com dados sintéticos, não tendo ocorrido contato com a administração, auditores (PwC), clientes ou fornecedores. Assim, **este trabalho acadêmico não configura auditoria real e não emite opinião profissional de auditor independente** sobre as demonstrações contábeis da Movida Participações S.A.
