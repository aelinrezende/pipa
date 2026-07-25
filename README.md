# pi-discovery

O `pi-discovery` é um pacote de distribuição focado em **Product Discovery**, **Engenharia de Requisitos** e **Especificação de Projetos**. Ele injeta inteligência de negócios no [Pipa Core](https://github.com/aelinrezende/pipa), transformando a orquestradora genérica em um verdadeiro esquadrão ágil de produto.

Ao invés de programar código-fonte, este pacote é focado em transformar *briefings* caóticos e ideações em especificações técnicas precisas, arquitetura de software, fluxos de UX e backlogs estruturados.

## 📦 Instalação

Adicione o pacote nas configurações do seu Pi (`settings.json` ou `package.json`):

```json
"packages": [
  "git:github.com/pipalabs/pi-discovery"
]
```

## 🚀 Como Funciona

Ao ser carregado, a arquitetura base da Pipa (Pipa Core) detecta este pacote e configura o ambiente local (`.pi/`) com as regras de domínio exclusivas para a área de Produto, trazendo um "Squad Hiper-Especializado" completo.

### 👑 A Liderança (Barbara - PM)
A Pipa incorpora a persona da **Barbara (Product Manager)**. A Barbara é a líder estratégica do Discovery: ela recebe os *briefs* iniciais, define o escopo geral, coordena o time de especificação e valida as entregas finais antes de entregar para o desenvolvimento. A Barbara não faz o trabalho braçal — ela delega.

### 🤝 O Squad de Discovery (Teammates)
Para extrair a especificação perfeita, a Barbara conta com o seguinte esquadrão:

1. **Isa (Product Owner):** A tradutora do negócio. Ela pega o brief da Barbara e escreve as **regras de negócio** detalhadas, descrevendo atores, fluxos e condições sem ambiguidade.
2. **Hugo (Arquiteto de Soluções):** O designer do sistema. Baseado nas regras da Isa, ele mapeia a **arquitetura**, definindo módulos, endpoints de API e contratos de dados (DTOs).
3. **Pamela (UX Designer):** A defensora do usuário. Ela mapeia as jornadas e descobre as **interfaces implícitas** (ex: telas de erro, confirmações e fluxos que não estavam explícitos nas regras).
4. **Stephanie (Tech Lead):** A avaliadora de risco. Ela lê a arquitetura definida pelo Hugo e elabora uma análise de **complexidade técnica**, apontando riscos e sugerindo a alocação ideal de desenvolvedores.
5. **Gabriel (Agile Master):** O organizador. Ele pega tudo o que foi validado e quebra em tarefas atômicas, estruturando um **backlog final (CSV)** com estimativas de tempo e dependências prontas para a *sprint*.

## 🛠️ Utilização Prática

1. Inicie a sessão passando o briefing cru do cliente para a **Barbara**.
2. A Barbara irá invocar a **Isa** para detalhar as regras de negócio.
3. Com as regras prontas, ela coordenará o trabalho entre **Pamela**, **Hugo** e **Stephanie** para mapear UX, Arquitetura e Complexidade.
4. Por fim, o **Gabriel** será acionado para tabular o esforço em um backlog.
5. A Barbara faz a revisão final e te entrega os artefatos prontos (Regras, Arquitetura, UX, Backlog e Análise de Risco) na pasta `.pi/artifacts/`.
