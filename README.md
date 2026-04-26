## 📌 Visão Geral do Sistema

O **MetaForce** é um sistema de negociação quantitativa de alta frequência e tomada de decisão autônoma. Diferente de robôs baseados em regras estáticas, ele opera como um organismo híbrido que une Deep Learning, microestrutura de mercado (Order Flow) e filtros aeroespaciais para operar simultaneamente nos mercados de Criptomoedas (WebSockets/API) e Ações/Índices Globais (MetaTrader 5).

---

## 🧠 Arquitetura Core: Os 7 Pilares de Engenharia

A inteligência do MetaForce baseia-se num funil de decisão multicamadas:

1. **Cérebro Adaptativo (Continuous Learning):** O núcleo preditivo é uma rede **LSTM-Transformer**. Através de um processo de "Sono REM", o modelo re-treina os seus tensores autonomamente todas as noites (`23:50`), otimizando os pesos para o regime de mercado do dia atual.
2. **Visão de Microestrutura (Order Book Imbalance - OBI):** Consome dados de Nível 2 do Livro de Ofertas. Se a rede neural sugerir compra, mas o cálculo de OBI detetar liquidez predatória (uma parede de vendas oculta por grandes players), a ordem é instantaneamente abortada.
3. **Filtro de Kalman (Redução de Ruído):** Implementação de matemática de rastreamento para suavizar o *Price Action* em tempo real, tornando a IA imune a manipulações intradiárias (*Stop Hunts*) e *spikes* de latência.
4. **Oráculo de Sentimento (NLP):** Módulo de Processamento de Linguagem Natural (VADER) integrado a feeds financeiros globais, calibrando o nível de confiança e o tamanho do lote de acordo com as métricas de *Fear & Greed*.
5. **Consciência Macroeconómica:** Mapeamento em tempo real do relógio do Federal Reserve (EUA). O motor de execução bloqueia o acesso ao mercado minutos antes de eventos de alta volatilidade (NFP, reuniões do FOMC) para proteger o capital.
6. **Gestão de Risco Evolutiva:** Dimensionamento de posição calculado via **Critério de Kelly** com alvos dinâmicos baseados na volatilidade real via **ATR (Average True Range)**.
7. **Escudo Assimétrico (Trailing em Múltiplas Fases):** Sistema avançado de gestão de operações em tempo real que tranca o *Break-even* aos primeiros sinais de lucro (cobrindo taxas institucionais) e cria um distanciamento elástico para surfar grandes tendências (*Trend Hunting*).

---

## 📸 Operacionalização e Telemetria (Evidências)

Embora a base de código seja fechada, o sistema opera sob rigorosa monitorização remota. Abaixo, exemplos da infraestrutura em ação:

### 1. O Motor em Ação (Logs de Execução)
*Nesta secção, observamos o sistema de Raio-X (OBI) filtrando entradas perigosas e a confirmação do Fine-Tuning noturno do PyTorch.*
<img width="1350" height="609" alt="Captura de tela 2026-04-25 214213" src="https://github.com/user-attachments/assets/24a3bf52-d3ec-444e-aa53-d23a9e416857" />
<img width="1309" height="668" alt="Captura de tela 2026-04-25 214110" src="https://github.com/user-attachments/assets/73d4336c-3f08-4283-bc86-7d5eb2194578" />

### 2. Telemetria e Relatórios (Integração Telegram)
*O MetaForce não exige que o operador olhe para gráficos. Toda a gestão, alertas macroeconômicos e relatórios de fecho de mercado são processados via interface assíncrona do Telegram Bot.*
<img width="720" height="1433" alt="image" src="https://github.com/user-attachments/assets/21522fb9-3cc6-413a-966e-2404f3e9a22b" />


---

## 🛠️ Stack Tecnológica

- **Backend / Core:** Python 3.12+ (Asyncio para operações não-bloqueantes)
- **Machine Learning / IA:** PyTorch, NumPy, Pandas, Scikit-learn
- **Mercados & Conectores:** Integração nativa `MetaTrader5` (Ações/Forex) e `ccxt` (Cripto/WebSockets)
- **Métricas & Dados:** TA-Lib, Pandas-TA, VADER (NLP)
- **Persistência de Dados:** SQLite (State Management para *Fault Tolerance*)
- **Telemetria:** Loguru, Telegram Bot API

---

## 📞 Conexão e Networking

Transformar teoria, matemática pura e dezenas de bibliotecas Python num ecossistema financeiro que opera de forma autônoma tem sido o desafio técnico mais recompensador da minha trajetória profissional como desenvolvedor de software.

Sempre em busca de otimização de execução, redução de latência e modelos preditivos mais robustos. Se alguém da área quantitativa, engenharia de dados ou instituições financeiras quiser trocar ideias sobre **arquiteturas orientadas a eventos** ou **otimização de tensores**, a caixa de mensagens está sempre aberta! ☕💻

**Wesley (Senhor Stone)**
*Estudante de Análise e Desenvolvimento de Sistemas | Desenvolvedor Backend & Quant*
* **LinkedIn:** [Acesse o meu Perfil](www.linkedin.com/in/wesley-fernandes-html)
* **Email:** [Wesleyffrr47@gmail.com]
