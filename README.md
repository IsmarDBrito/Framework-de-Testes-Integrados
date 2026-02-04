# 🚀 Framework de Testes Integrados - Urban Scooter

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![QA](https://img.shields.io/badge/QA-Testing-blue.svg)](https://github.com/IsmarDBrito/Framework-de-Testes-Integrados)

Framework completo de testes automatizados para a aplicação **Urban Scooter**, cobrindo testes integrados para **Web**, **Mobile** e **API**.

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Características](#características)
- [Tecnologias](#tecnologias)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Como Usar](#como-usar)
- [Executando os Testes](#executando-os-testes)
- [Relatórios](#relatórios)
- [Contribuindo](#contribuindo)
- [Licença](#licença)
- [Autor](#autor)

## 🎯 Sobre o Projeto

Este framework foi desenvolvido para garantir a qualidade e confiabilidade da aplicação Urban Scooter através de testes automatizados integrados. O projeto abrange três principais frentes de teste:

- **🌐 Testes Web**: Interface web responsiva e funcionalidades do frontend
- **📱 Testes Mobile**: Aplicativos mobile (iOS/Android) e funcionalidades nativas
- **🔌 Testes API**: Endpoints RESTful, validação de contratos e integrações

## ✨ Características

- ✅ **Testes Integrados**: Cobertura completa Web + Mobile + API
- 🔄 **CI/CD Ready**: Integração com pipelines de deploy
- 📊 **Relatórios Detalhados**: Geração automática de relatórios de execução
- 🎨 **Page Object Model**: Arquitetura organizada e manutenível
- 🔐 **Testes de Segurança**: Validação de autenticação e autorização
- 📈 **Performance Testing**: Testes de carga e performance
- 🌍 **Cross-browser**: Suporte para múltiplos navegadores
- 📱 **Cross-platform**: Suporte para iOS e Android

## 🛠 Tecnologias

### Testes Web
- **Selenium WebDriver** / **Playwright** - Automação de navegadores
- **Cypress** - Framework de testes end-to-end
- **Jest** / **Mocha** - Framework de testes

### Testes Mobile
- **Appium** - Automação mobile cross-platform
- **Detox** - Framework para React Native
- **Espresso** / **XCUITest** - Testes nativos

### Testes API
- **REST Assured** / **Supertest** - Testes de API REST
- **Postman** / **Newman** - Testes de API e collections
- **Karate** - Framework BDD para testes de API

### Ferramentas Auxiliares
- **Allure** / **Mochawesome** - Geração de relatórios
- **Docker** - Containerização de ambientes
- **GitHub Actions** / **Jenkins** - CI/CD
- **TypeScript** / **JavaScript** - Linguagens de programação

## 📦 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- **Node.js** (v18 ou superior)
- **npm** ou **yarn**
- **Java JDK** (v11 ou superior) - para Appium
- **Android Studio** / **Xcode** - para testes mobile
- **Docker** (opcional) - para ambientes containerizados
- **Git**

## 🚀 Instalação

1. **Clone o repositório**
```bash
git clone https://github.com/IsmarDBrito/Framework-de-Testes-Integrados.git
cd Framework-de-Testes-Integrados
```

2. **Instale as dependências**
```bash
npm install
# ou
yarn install
```

3. **Configure as variáveis de ambiente**
```bash
cp .env.example .env
# Edite o arquivo .env com suas configurações
```

4. **Instale dependências do Appium** (para testes mobile)
```bash
npm install -g appium
appium driver install uiautomator2  # Android
appium driver install xcuitest      # iOS
```

## 📁 Estrutura do Projeto

```
Framework-de-Testes-Integrados/
│
├── 📁 tests/
│   ├── 📁 web/              # Testes web
│   │   ├── 📁 e2e/         # Testes end-to-end
│   │   ├── 📁 integration/ # Testes de integração
│   │   └── 📁 pages/       # Page Objects
│   │
│   ├── 📁 mobile/          # Testes mobile
│   │   ├── 📁 android/     # Testes Android
│   │   ├── 📁 ios/         # Testes iOS
│   │   └── 📁 shared/      # Código compartilhado
│   │
│   └── 📁 api/             # Testes de API
│       ├── 📁 endpoints/   # Testes de endpoints
│       ├── 📁 contracts/   # Testes de contrato
│       └── 📁 integration/ # Testes de integração
│
├── 📁 config/              # Arquivos de configuração
│   ├── webdriver.config.js
│   ├── appium.config.js
│   └── api.config.js
│
├── 📁 utils/               # Utilitários e helpers
├── 📁 reports/             # Relatórios gerados
├── 📁 docs/                # Documentação
│
├── 📄 package.json
├── 📄 .env.example
└── 📄 README.md
```

## 💻 Como Usar

### Executando Testes Web

```bash
# Executar todos os testes web
npm run test:web

# Executar testes em modo headless
npm run test:web:headless

# Executar testes em um navegador específico
npm run test:web:chrome
npm run test:web:firefox
```

### Executando Testes Mobile

```bash
# Executar testes Android
npm run test:mobile:android

# Executar testes iOS
npm run test:mobile:ios

# Executar testes em dispositivo específico
npm run test:mobile:android -- --device="emulator-5554"
```

### Executando Testes API

```bash
# Executar todos os testes de API
npm run test:api

# Executar testes de um endpoint específico
npm run test:api -- --grep "users"

# Executar com ambiente específico
npm run test:api -- --env=staging
```

### Executando Todos os Testes

```bash
# Executar suite completa (Web + Mobile + API)
npm run test:all

# Executar com relatório detalhado
npm run test:all -- --reporter=allure
```

## 📊 Relatórios

Os relatórios são gerados automaticamente após a execução dos testes:

- **Allure Reports**: `npm run report:allure`
- **HTML Reports**: Disponível em `reports/html/`
- **JSON Reports**: Disponível em `reports/json/`

Para visualizar o relatório Allure:
```bash
npm run report:allure:serve
```

## 🔧 Configuração

### Variáveis de Ambiente

Configure as seguintes variáveis no arquivo `.env`:

```env
# Ambiente
NODE_ENV=development

# URLs
WEB_URL=https://urbanscooter.com
API_URL=https://api.urbanscooter.com
MOBILE_APP_PATH=./apps/urbanscooter.apk

# Credenciais
API_KEY=your_api_key
TEST_USER_EMAIL=test@example.com
TEST_USER_PASSWORD=password123

# Configurações Mobile
ANDROID_DEVICE_NAME=emulator-5554
IOS_DEVICE_NAME=iPhone 14
APPIUM_SERVER_URL=http://localhost:4723

# Relatórios
ALLURE_RESULTS=./allure-results
REPORT_PATH=./reports
```

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Para contribuir:

1. Faça um **fork** do projeto
2. Crie uma **branch** para sua feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. **Push** para a branch (`git push origin feature/AmazingFeature`)
5. Abra um **Pull Request**

### Padrões de Código

- Siga os padrões de código estabelecidos no projeto
- Escreva testes claros e bem documentados
- Adicione comentários quando necessário
- Mantenha a cobertura de testes acima de 80%

## 📝 Exemplos de Testes

### Exemplo: Teste Web (Login)

```javascript
describe('Login Page', () => {
  it('should login successfully with valid credentials', async () => {
    await loginPage.navigate();
    await loginPage.enterEmail('user@example.com');
    await loginPage.enterPassword('password123');
    await loginPage.clickLogin();
    
    expect(await dashboardPage.isDisplayed()).toBe(true);
  });
});
```

### Exemplo: Teste Mobile (Navegação)

```javascript
describe('Mobile Navigation', () => {
  it('should navigate to profile screen', async () => {
    await homeScreen.tapProfileButton();
    expect(await profileScreen.isDisplayed()).toBe(true);
  });
});
```

### Exemplo: Teste API (GET Request)

```javascript
describe('Users API', () => {
  it('should return user list', async () => {
    const response = await api.get('/users');
    
    expect(response.status).toBe(200);
    expect(response.data).toHaveProperty('users');
    expect(Array.isArray(response.data.users)).toBe(true);
  });
});
```

## 🐛 Troubleshooting

### Problemas Comuns

**Erro: Appium não encontrado**
```bash
npm install -g appium
appium --version
```

**Erro: WebDriver não inicializa**
- Verifique se o ChromeDriver está atualizado
- Confirme que o caminho do driver está correto

**Erro: Dispositivo mobile não detectado**
```bash
adb devices  # Para Android
xcrun simctl list devices  # Para iOS
```

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor

**Ismar D. Brito**

- GitHub: [@IsmarDBrito](https://github.com/IsmarDBrito)
- LinkedIn: [Ismar D. Brito](https://linkedin.com/in/ismardbrito)

## 🙏 Agradecimentos

- Equipe Urban Scooter
- Comunidade de QA e Testing
- Todos os contribuidores do projeto

---

⭐ Se este projeto foi útil para você, considere dar uma estrela!
