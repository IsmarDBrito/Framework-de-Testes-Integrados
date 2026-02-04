# Framework de Testes Integrados - Urban Scooter

Documentação do framework de testes para a aplicação **Urban Scooter**, cobrindo testes para **Web**, **Mobile** e **API**.

## 📋 Sobre o Projeto

Este projeto contém a documentação e casos de teste para validação da aplicação Urban Scooter. Os testes foram desenvolvidos seguindo uma abordagem prática e direta, cobrindo as principais funcionalidades em três frentes:

- **🌐 Testes Web**: Validação da interface web e funcionalidades do frontend com testes Cross-browser (Chrome/Opera)
- **📱 Testes Mobile**: Validação de aplicativos mobile (iOS/Android)
- **🔌 Testes API**: Validação de contratos, códigos de status (HTTP Status Codes) e integridade de dados via endpoints REST

**Metodologia**: Aplicação de técnicas de Classes de Equivalência, Valores Limite e testes Cross-browser (Chrome/Opera).

## 📁 Estrutura

O projeto está organizado de forma simples e objetiva:

```
Framework-de-Testes-Integrados/
│
├── 📄 Documentação de Testes (Excel)
│   └── Casos de teste organizados por módulo
│
└── 📄 README.md
```

## 🔄 Fluxo de Trabalho de QA

O processo de qualidade segue um fluxo estruturado desde a análise de requisitos até a gestão de defeitos no Jira:

```
┌─────────────────────────────────────────────────────────────────┐
│  1. ANÁLISE DE REQUISITOS                                      │
│     ↓ Análise de especificações e documentação                 │
└─────────────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────────┐
│  2. PLANEJAMENTO DE TESTES                                     │
│     • Definição de estratégia de teste                         │
│     • Criação de casos de teste (Classes de Equivalência)      │
│     • Identificação de valores limite                           │
└─────────────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────────┐
│  3. EXECUÇÃO DE TESTES                                         │
│     • Testes Web (Cross-browser: Chrome/Opera)                  │
│     • Testes Mobile (iOS/Android)                               │
│     • Testes API (Validação de contratos e status codes)       │
└─────────────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────────┐
│  4. IDENTIFICAÇÃO DE DEFEITOS                                  │
│     • Documentação detalhada do bug                             │
│     • Evidências (screenshots, logs, requests/responses)        │
│     • Classificação por severidade e prioridade                 │
└─────────────────────────────────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────────┐
│  5. GESTÃO NO JIRA                                             │
│     • Criação de ticket com informações completas               │
│     • Rastreabilidade: Requisito → Caso de Teste → Bug         │
└─────────────────────────────────────────────────────────────────┘
```

## 📝 Documentação

A documentação completa dos casos de teste está disponível no arquivo Excel incluído no projeto, contendo:

- Casos de teste para Web
- Casos de teste para Mobile  
- Casos de teste para API
- Cenários de teste e resultados esperados
- **Rastreabilidade**: Gestão completa do ciclo de vida de defeitos com integração direta ao Jira

## 🐛 Principais Descobertas (Bugs Críticos)

Durante a execução dos testes, foram identificados e reportados os seguintes bugs críticos:

| Plataforma | Descrição do Bug | Impacto | Status |
|------------|------------------|---------|--------|
| **API** | Falha na validação de caracteres especiais no endpoint de cadastro (Status 201 retornado em vez de 400) | Alto - Permite dados inválidos no sistema | Reportado no Jira |
| **Mobile** | Bug de persistência no alerta de rede quando o dispositivo alterna para orientação horizontal | Médio - UX comprometida em rotação | Reportado no Jira |
| **Web** | Erro de validação no campo "Nome" ao aceitar caracteres não latinos sem o devido tratamento | Alto - Dados inconsistentes no banco | Reportado no Jira |

Todos os bugs foram documentados com evidências completas (screenshots, logs, requests/responses) e rastreados no Jira com links diretos para os casos de teste relacionados.

## 👤 Autor

**Ismar D. Brito**

- GitHub: [@IsmarDBrito](https://github.com/IsmarDBrito)
- LinkedIn: https://www.linkedin.com/in/ismar-de-brito-costa-junior-6ab5b0377/

