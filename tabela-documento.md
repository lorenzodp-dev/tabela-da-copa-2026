# 📊 Tabela da Copa do Mundo de 2026

## 1. Nome
**Tabela da Copa do Mundo de 2026**

## 2. Versão
**v1.0**

---

## 3. Escopo

### 🎯 Objetivo
Desenvolver uma tabela intuitiva e atualizada para os interessados, considerando que atualmente muitas tabelas na internet demoram até dias para atualizar os resultados.

### 👥 Público-alvo
Todos os interessados na Copa do Mundo de 2026.

### ⚠️ Limitações
- (Definir o que o sistema não fará)

---

## 4. Requisitos Funcionais (RF)

### RF-01: Gestão de grupos
O sistema deve permitir o cadastro de grupos de A a L.

### RF-02: Gestão de seleções
O sistema deve permitir o cadastro das 48 seleções, incluindo:
- Nome  
- Bandeira  
- Abreviação  
- Grupo  

**Regra:**  
O grupo deve ser selecionado a partir do cadastro de grupos existente.

---

### RF-03: Gestão de Sedes
O sistema deve permitir cadastro das sedes, incluindo:
- Nome do país  
- Cidade  
- Estádio  
- Capacidade do estádio  

---

### RF-04: Gestão de Partidas
O sistema deve permitir cadastro das partidas, incluindo:
- Data  
- Horário  
- Sede  
- Seleção mandante  
- Seleção visitante  

**Regras:**
- A sede deve ser selecionada
- As seleções devem ser selecionadas

---

### RF-05: Tabela das partidas
O sistema deve permitir a criação da tabela para visualização.

**Regras:**
- Organização por grupo
- Ordem cronológica
- Classificação correta é obrigatória

---

### RF-06: Resultados das Partidas
Permitir inclusão de resultados com quantidade de gols.

**Regras:**
- Valores devem ser ≥ 0

---

### RF-07: Classificação
Permitir visualização do ranking por grupo.

**Critérios:**
1. Pontuação  
2. Vitórias  
3. Saldo de gols  
4. Outros critérios a definir  

---

### RF-08: Avanço de Fases
O sistema deve calcular os classificados.

**Regras:**
- 2 primeiros de cada grupo → 24 seleções  
- 8 melhores restantes → total de 32 seleções  
- Outras regras a definir  

---

## 5. Requisitos Não Funcionais (RNF)
- (A definir)

---

## 6. Diagramas UML

### 6.1 Diagramas de Classe
- (A definir)

### 6.2 Diagramas de Casos de Uso
- (A definir)

---

## 7. Modelo de Dados (MER)
- (A definir)

---

## 8. Arquitetura

- MVC  
- Monolito  
- Microsserviços  
- REST  
- Camadas:
  - Apresentação  
  - Regra de Negócio  
  - Dados  

---

## 9. Plano de Testes
- (A definir)

---

## 10. Cronograma
- (A definir)

---

## 11. DevOps e Implantação

- Versionamento: Git  
- Estratégia de Backup  
- Ambiente de Produção:
  - Local  
  - Cloud  
  - VPS  
  - Docker  
  - Hospedagem compartilhada  

---

## 12. Segurança e LGPD

### Política de Privacidade
- Quais dados serão coletados  
- Como os dados serão utilizados  

### Proteção de Dados
(Apenas para pessoas físicas)

**Modelo de ameaça:**
Ameaça = Agente + Mecanismo + Ativo  

- Lista de ameaças  
- Estratégias de mitigação  

---

## 13. Investimento

**Fórmula:**
Investimento = horas * valor da hora

---

# 📌 Análise de Requisitos

## CRUD
- Create → Incluir  
- Read → Consultar  
- Update → Alterar  
- Delete → Excluir  

---

# 🧠 Entidades (Banco de Dados)

## Classe: Seleção
- Nome (chave candidata – não recomendada)  
- Bandeira  
- Abreviação (PRIMARY KEY)  
- Grupo  

---

## Classe: Grupo
- ID (int)  
- Nome (string)  
- Fase (string)  

---

## Classe: Sede
- ID (PRIMARY KEY)  
- País  
- Cidade  
- Estádio  
- Capacidade  

---

## Classe: Partida
- ID (int)  
- Data (date)  
- Horário (time)  
- Sede (FK → Sede.id)  
- Time visitante (FK → Seleção.abreviação)  
- Time mandante (FK → Seleção.abreviação)  

---

**Regra importante:**
IDs NÃO podem se repetir.

---

# ⚙️ Requisitos Técnicos

## 💻 Desktop
- Linguagem: C# (Visual Studio 2022)  
- Banco: PostgreSQL  
- Sistema: Windows 10+  

---

## 🌐 Web

### Front-end
- HTML, CSS, JavaScript, React  

### Back-end
- Node.js, JavaScript, PHP (opcional)  

### Banco de Dados
- MySQL ou MariaDB  

### Infraestrutura
- Hospedagem (1 vCPU, 2GB RAM, 50GB storage)  
- Domínio (registro.br)  
- Segurança (Cloudflare ou similar)  

---

## 📱 Mobile
- Linguagem: React Native  
- Banco: via API  
- Ambiente: Expo  