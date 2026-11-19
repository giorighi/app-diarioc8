# Design System — Calculadora Financeira 12C RPN (Android / Google Play)

## 1. Visão Geral e Identidade Visual
- **Conceito:** Precisão institucional e clareza tátil. Une a sobriedade do mercado financeiro (azul-marinho e branco) ao contraste funcional inspirado nas calculadoras financeiras clássicas (dourado suave para funções secundárias e verde para confirmação/visor).
- **Plataforma Alvo:** Android (Google Play Store), otimizado para uso mobile em modo retrato (portrait) e paisagem (landscape) com toque rápido sem atraso.
- **Identidade de Canal:** Assinatura discreta `@diarioc8` integrada ao cabeçalho/moldura da calculadora, conectando a ferramenta à página de finanças no Instagram sem nomes pessoais (compliance-ready).

---

## 2. Paleta de Cores (Color Tokens)

### Cores Principais (Brand & Surfaces)
| Token | Nome | Hex | Uso na Interface |
| :--- | :--- | :--- | :--- |
| `--color-navy-900` | Azul-Marinho Profundo | `#0B192C` | Fundo principal do app, barra de navegação superior/inferior e moldura externa |
| `--color-navy-800` | Azul-Marinho Corpo | `#132743` | Superfície dos botões numéricos (`0-9`) e cartões de abas extras |
| `--color-navy-700` | Azul-Marinho Operações | `#1E3A5F` | Botões de funções financeiras (`n`, `i`, `PV`, `PMT`, `FV`) e operadores (`+`, `-`, `×`, `÷`) |
| `--color-white-100` | Branco Puro | `#FFFFFF` | Texto principal sobre teclas escuras, ícones de ação e cartões de exportação |
| `--color-white-200` | Branco Gelo / Off-White | `#F4F6F9` | Texto secundário e fundo claro para tabelas de cronograma e relatórios exportados |

### Cores de Destaque e Função (Accents & Shift Keys)
| Token | Nome | Hex | Uso na Interface |
| :--- | :--- | :--- | :--- |
| `--color-gold-500` | Amarelo Levemente Dourado | `#D4AF37` | Tecla de shift `f`, legendas superiores (`PRICE`, `YTM`, `SL`, `SOYD`, `DB`, `REG`, `FIN`, `AMORT`) e assinatura `@diarioc8` |
| `--color-gold-400` | Dourado Suave Hover/Active | `#E6C252` | Estado pressionado da tecla `f` e aba ativa na navegação |
| `--color-green-500` | Verde Esmeralda | `#1F8A5B` | Tecla `ENTER`, botões de compartilhamento/exportação e indicadores positivos |
| `--color-green-lcd` | Verde Visor Clássico | `#D8E2DC` | Fundo do visor LCD de alto contraste |
| `--color-green-lcd-text` | Verde-Escuro LCD | `#0B192C` | Dígitos principais do visor para leitura nítida sob luz solar ou escritório |

### Cores Semânticas (Feedback)
| Token | Nome | Hex | Uso |
| :--- | :--- | :--- | :--- |
| `--color-sky-shift` | Azul Claro (`g` Shift) | `#5BA4E6` | Tecla `g` e legendas inferiores (`DATE`, `ΔDYS`, `D.MY`, `M.DY`, `BEG`, `END`) |
| `--color-error` | Coral Alerta | `#D9534F` | Mensagens de erro (`Error 0`, `Error 5`, `Error 8`) e tecla `CLX` |

---

## 3. Tipografia
- **Visor Numérico (LCD):** `JetBrains Mono` ou `Roboto Mono` — `Bold`, tabular figures (`font-variant-numeric: tabular-nums`), tamanho `28sp` a `34sp` para alinhamento perfeito de casas decimais.
- **Rótulos das Teclas Principais:** `Inter` ou `Roboto` — `SemiBold`, `14sp` a `16sp`, cor `#FFFFFF`.
- **Legendas Shift (`f` e `g`) e Handle `@diarioc8`:** `Inter` ou `Roboto` — `Bold`, `9sp` a `11sp`, tracking `+0.5px`.

---

## 4. Arquitetura de Telas e Abas Extras (Navigation)

### A. Cabeçalho Minimalista (Top Bar)
- Fundo `--color-navy-900` (`#0B192C`).
- **Esquerda:** Título `12C FINANCIAL` em branco com a marca d'água/handle **`@diarioc8`** logo abaixo ou ao lado em `--color-gold-500` (`#D4AF37`).
- **Direita (Ações Rápidas):**
  1. **Botão Atalho Google Finance:** Ícone discreto de gráfico/mercado com rótulo `Google Finance` (abre `https://www.google.com/finance` ou dispara intent para o app Google Finance no Android para consulta rápida de cotações, taxas e índices).
  2. **Botão Compartilhar / Exportar Cálculo:** Ícone de compartilhamento em `--color-green-500` (`#1F8A5B`) que abre o modal de memória de cálculo.

### B. Barra de Abas Extras (Bottom / Top Tab Navigation)
Navegação em abas sobre fundo `--color-navy-900` com indicador ativo em `--color-gold-500`:
1. **Aba 1 — `Calculadora` (Principal):**
   - Visor LCD (`--color-green-lcd`), fita da pilha RPN (`Y`, `Z`, `T`, `LSTx`) e teclado tátil completo com TVM, Datas (`DATE`, `ΔDYS`), Bonds (`PRICE`, `YTM`) e Depreciação (`SL`, `SOYD`, `DB`).
2. **Aba 2 — `Fluxo de Caixa` (`CF0 / NPV / IRR`):**
   - Lista visual editável de fluxos (`CF0`, `CF1..CFn` e repetições `Nj`), taxa de desconto (`i`) e cálculo instantâneo de **VPL (`NPV`)** e **TIR (`IRR`)**, sincronizado com os registradores da calculadora.
3. **Aba 3 — `Depreciação & Bonds` (Cronograma):**
   - Tabela ano a ano comparando **Linha Reta (`SL`)**, **Soma dos Dígitos (`SOYD`)** e **Saldo Decrescente (`DB`)** (mostrando quota anual, depreciação acumulada e valor contábil residual), além de detalhamento de **Cupom Corrido (`AI`)** e **Preço Limpo/Sujo** para títulos.
4. **Aba 4 — `Amortização` (`Price / SAC`):**
   - Simulador de cronograma parcela a parcela comparando **Tabela Price** e **SAC** (prestação, juros, amortização e saldo devedor), integrado com a função `f + AMORT`.

---

## 5. Funcionalidade: Exportar, Baixar e Compartilhar Raciocínio de Cálculo

### Fluxo e Comportamento (Modal "Memória de Cálculo")
Toda operação financeira executada (TVM, Datas, Bonds, Depreciação, VPL/TIR ou Amortização) registra automaticamente o **passo a passo lógico** em uma fita de auditoria interna. Ao tocar no botão **Exportar / Compartilhar**:

1. **Pré-visualização do Raciocínio Estruturado:**
   Exibe um cartão limpo (fundo `#FFFFFF`, cabeçalho `#0B192C` com `@diarioc8`) contendo:
   - **Tipo de Cálculo & Data/Hora** (ex.: *Precificação de Título — Actual/Actual* ou *Depreciação DB*).
   - **Premissas Inseridas:** Valores exatos de cada registrador (`PV`, `FV`, `PMT`, `i`, `n`, datas, convenção `D.MY`/`M.DY`, modo `BEG`/`END`).
   - **Raciocínio / Fita RPN:** Sequência lógica e fórmula aplicada até chegar ao resultado.
   - **Resultado Final Destacado:** Em verde esmeralda (`#1F8A5B`) com assinatura discreta `Calculado via 12C Financial · @diarioc8`.
2. **Ações Disponíveis no Modal:**
   - **Compartilhar Direto (Android Share Sheet):** Envia o resumo formatado em texto (para WhatsApp, Telegram, E-mail ou Instagram Direct) ou como card de imagem PNG pronto para Stories/Feed.
   - **Fazer Download:** Salva localmente no dispositivo em dois formatos à escolha do usuário:
     - **`.PDF` / `.PNG`:** Relatório visual limpo com a paleta azul-marinho, dourado e branco.
     - **`.CSV` / `.TXT`:** Para abrir direto no Excel / Google Sheets (especialmente útil para as abas de cronograma de Depreciação, Amortização e Fluxo de Caixa).
   - **Copiar Raciocínio:** Copia o texto estruturado para a área de transferência com um toque.

---

## 6. Diretrizes de Usabilidade para Google Play
1. **Área de Toque (Touch Target):** Altura mínima de `44dp` por tecla com espaçamento de `4dp` entre botões para evitar toques acidentais em telas de 5.5" a 6.7".
2. **Modo Offline Nativo:** Zero dependência de rede para cálculos; todos os motores (TVM, Datas, Bonds, Depreciação, Cronogramas e geração local de exportação) rodam 100% offline. O link para o **Google Finance** abre externamente apenas quando tocado pelo usuário.
3. **Acessibilidade:** Contraste mínimo de `7:1` entre fundo e texto nas teclas principais e no visor LCD.