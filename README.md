# Estudo Dirigido: Controle e Automação com Foco em Indústria 4.0

## Plano de Estudo: Semestre 2025.2
**Disciplina:** Controle e Automação

**Professor:** Moacy Pereira da Silva

**Alunos:** Caio Lívio Leite Muniz Dantas, Vinícius Gonzaga CavalcanteRodrigues

Este repositório contém os resumos estruturados, notebooks de simulação em Python (Google Colab) e relatórios de integração com a Indústria 4.0, conforme as diretrizes do Estudo Dirigido. O projeto estabelece uma ponte entre os fundamentos teóricos do controle clássico (Dorf & Bishop) e as tecnologias modernas da Quarta Revolução Industrial.

---

## 🎯Objetivo Principal

Consolidar os conceitos fundamentais de Sistemas de Controle através de simulações e estudos aplicados, com **ênfase na conexão com tecnologias de Indústria 4.0** (MES, PIMS, APC, RTO, IIoT e Digital Twin).

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Finalidade |
| :--- | :--- |
| **Python** | Linguagem principal para simulações. |
| **Google Colab (.ipynb)** | Ambiente de desenvolvimento para execução e visualização de simulações interativas. |
| **Biblioteca `control`** | Implementação de Funções de Transferência, análise de estabilidade e resposta no tempo. |
| **LaTeX / Markdown** | Formatação de relatórios e documentação científica. |

---

## 🗺️ Estrutura do Conteúdo

O projeto está organizado por capítulos do livro "Sistemas de Controle Moderno" (Dorf & Bishop), com foco nos fundamentos e sua relevância industrial.

### 1. 📂 `Capitulo_4_Caracteristicas_Realimentacao`

Focado nas vantagens inerentes da realimentação negativa (malha fechada).

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_4.md` | Resumo dos conceitos de sensibilidade, rejeição de perturbação e o custo da realimentação. | **Sensibilidade** ($S(s)$), **Função Sensibilidade Complementar** ($C(s)$), **Compromisso de Frequência** (Alto ganho em baixa frequência para rejeitar perturbações, baixo ganho em alta frequência para atenuar ruído). |
| `Notebook_Sensibilidade_Rejeicao.ipynb` | Simulações em Python demonstrando a redução drástica da sensibilidade do sistema a variações paramétricas ($G(s)$) em malha fechada, e o efeito do ganho na rejeição de perturbações. |
| `Relatorio_I40_Cap4.md` | Conexão entre a **Robustez** do controle e **APC/RTO**, além da relação entre o ruído ($N(s)$) e os dados de **IIoT/Digital Twin**. |

### 2. 📂 `Capitulo_5_Desempenho_Sistemas`

Focado nas especificações quantitativas do desempenho no domínio do tempo.

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_5.md` | Métrica de desempenho, a correlação entre polos/zeros no plano $s$ e a resposta transitória. | **$M.U.P.$**, **$T_s$**, **Instante de Pico** ($T_p$), **Polos Dominantes**, **$e_{ss}$** (Tipo de Sistema). |
| `Notebook_Transitorio.ipynb` | Simulações da **Resposta ao Degrau** para diferentes fatores de amortecimento ($\zeta$), ilustrando o compromisso entre velocidade ($T_s$) e oscilação ($M.U.P.$). |
| `Notebook_Tipo_Erro.ipynb` | Simulações da resposta para entradas Degrau, Rampa e Parábola, quantificando o $e_{ss}$ para sistemas Tipo 0, Tipo 1 e Tipo 2. |
| `Relatorio_I40_Cap5.md` | Aplicação dos **Índices ITAE/ISE** na otimização de processos (APC) e a relevância de $T_s$ e $e_{ss}$ para a qualidade dos dados do **MES**. |

### 3. 📂 `Capitulo_6_Estabilidade_Lineares`

Focado na condição fundamental para a existência do sistema de controle.

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_6.md` | Conceitos de estabilidade absoluta e relativa, a relação entre polos/autovalores no semi-plano direito e o **Critério de Routh-Hurwitz**. | **Estabilidade absoluta**, **Marginalmente Estável**, **Tabela de Routh**, **Polinômio Auxiliar**, **Autovalores**. |
| `Notebook_Routh_Ganhos.ipynb` | Uso da função `roots` para calcular as raízes da equação característica em função de um parâmetro de ganho ($K$), visualizando a **margem de estabilidade** e o ponto onde os polos cruzam o eixo $j\omega$ (instabilidade). |
| `Relatorio_I40_Cap6.md` | Discussão da estabilidade em sistemas intrinsecamente instáveis (robótica) e o uso do **Routh-Hurwitz** e da **Análise de Polos** para garantir a segurança no **SIS** e no **Digital Twin**. |

### 4. 📂 `Capitulo_7_Metodo_Lugar_Raizes`

Focado na ferramenta gráfica para análise da trajetória dos polos de malha fechada e projeto de controladores através da variação de parâmetros (ganho $K$).

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_7.md` | Detalhamento do algoritmo gráfico, condições matemáticas para existência do lugar das raízes e regras de construção manual vs. computacional. | **Condição de Fase/Módulo**, **Assíntotas**, **Centróide** ($\sigma_A$), **Ponto de Separação** (*Breakaway*), **Estabilidade Relativa**. |
| `Notebook_Lugar_Raizes.ipynb` | Simulações utilizando `control.root_locus` para visualizar a estabilidade, desenhar assíntotas, analisar sistemas com **Atraso de Transporte (Padé)** e comparar controladores. | **Ganho Crítico** ($K_{crit}$), **Aproximação de Padé**, **Compensação** (Zeros e Polos adicionais), **Impacto do Ganho no Sobressinal**. |
| `Relatorio_I40_Cap7.md` | A aplicação do LGR na validação de arquiteturas em **DCS**, garantias de estabilidade para **SIS** (Safety Instrumented Systems) e uso em **Comissionamento Virtual**. | **Autotuning em CLPs**, **Digital Twin**, **Gain Scheduling**, **Segurança Funcional (SIL)**. |

### 5. 📂 `Capitulo_10_Projeto_Sistemas_Controle`

Focado na síntese de compensadores para alterar a resposta natural da planta e atender especificações rigorosas de desempenho.

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_10.md` | Metodologias para projeto de compensadores em cascata utilizando LGR e Resposta em Frequência (Bode). | **Compensador por Avanço (Lead)**, **Compensador por Atraso (Lag)**, **Atraso-Avanço**, **Sintonia PID (Ziegler-Nichols)**. |
| `Notebook_Projeto_Compensadores.ipynb` | Design passo a passo de controladores para melhorar $T_s$ e reduzir $M_p$. Comparação visual entre sistemas não compensados e compensados. | **Aumento da Largura de Banda**, **Margem de Fase (PM)**, **Margem de Ganho (GM)**, **Robustez**. |
| `Relatorio_I40_Cap10.md` | O papel do controle robusto na base da pirâmide de automação (Nível 0 e 1) e sua importância para o **APC** (Advanced Process Control). | **Controle de Movimento (Robótica)**, **Estabilidade de Processos Químicos**, **Integração com RTO**. |

### 6. 📂 `Capitulo_13_Sistemas_Controle_Digital`

Focado na discretização de controladores para implementação em computadores, microcontroladores e CLPs.

| Arquivo | Descrição | Conceitos-Chave |
| :--- | :--- | :--- |
| `Resumo_Capitulo_13.md` | A matemática por trás da amostragem de sinais e a estabilidade no domínio $z$. | **Transformada Z**, **Segurador de Ordem Zero (ZOH)**, **Teorema da Amostragem (Nyquist)**, **Mapeamento plano $s \to z$**. |
| `Notebook_Controle_Digital.ipynb` | Simulação da discretização de plantas contínuas e análise do efeito da taxa de amostragem ($T$) na estabilidade do sistema digital. | **Aliasing**, **Equações de Diferenças**, **Atraso de Computação**, **Resposta Digital vs. Analógica**. |
| `Relatorio_I40_Cap13.md` | Discussão sobre latência em redes industriais sem fio e processamento na borda (**Edge Computing**). | **Networked Control Systems**, **Protocolos Industriais**, **Latência em IIoT**. |

---

## 🏭 Entrega Final: Relatório Integrador Indústria 4.0

Esta seção consolida todo o conhecimento adquirido, conectando as equações diferenciais e funções de transferência às tecnologias habilitadoras da manufatura avançada.

**Arquivo Principal:** [`Relatorio_Final_Integrador.md`](Relatorio_Final_Integrador.md)

### Tópicos Abordados:

1.  **APC (Advanced Process Control):** Como o PID bem sintonizado (Cap. 10) é a fundação para o Controle Preditivo (MPC).
2.  **RTO (Real-Time Optimization):** A dependência da estabilidade do sistema para a otimização econômica em tempo real.
3.  **MES & PIMS:** A relação entre os vetores de simulação temporal ($y(t)$) e os bancos de dados históricos industriais (Historian).
4.  **Digital Twin:** O uso de modelos matemáticos e LGR (Cap. 7) para previsão de cenários e comissionamento virtual.
5.  **IIoT & Latência:** O impacto de redes sem fio e atrasos de transporte na estabilidade da malha de controle.

---

## 🚀 Como Executar os Notebooks

Para visualizar e interagir com as simulações desenvolvidas:

1.  Acesse a pasta do capítulo desejado.
2.  Clique no arquivo com extensão `.ipynb`.
3.  Para interagir (rodar o código), clique no botão **"Open in Colab"** no topo do arquivo (se disponível) ou baixe o arquivo para executar em seu ambiente Jupyter local.

**Dependências Python:**
* `control`
* `matplotlib`
* `numpy`
* `scipy`

---

## 📚 Referências Bibliográficas

* **DORF, Richard C.; BISHOP, Robert H.** *Sistemas de Controle Moderno*. 13ª Edição. Rio de Janeiro: LTC, 2018.
* **NISE, Norman S.** *Engenharia de Sistemas de Controle*. 7ª Edição. Rio de Janeiro: LTC, 2017.
* **OGATA, Katsuhiko.** *Engenharia de Controle Moderno*. 5ª Edição. São Paulo: Pearson, 2010.
