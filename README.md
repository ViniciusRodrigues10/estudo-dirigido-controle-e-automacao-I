# 📚 Estudo Dirigido: Controle e Automação com Foco em Indústria 4.0

## Plano de Estudo: Semestre 2025.2
**Disciplina:** Controle e Automação
**Professor:** Moacy Pereira da Silva

Este repositório contém os resumos estruturados, notebooks de simulação em Python (Google Colab) e relatórios de integração com a Indústria 4.0, conforme as diretrizes do Estudo Dirigido. O projeto estabelece uma ponte entre os fundamentos teóricos do controle clássico (Dorf & Bishop) e as tecnologias modernas da Quarta Revolução Industrial.

---

## 🎯 Objetivo Principal

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
