# AgroHive 🌱

AgroHive é uma plataforma de dados agrícolas que ajuda agricultores nas tomadas de decisões do dia a dia do campo, fornecendo informações climáticas em tempo real e análise por satélite da saúde das plantas.

## 🚀 Funcionalidades

- **📍 Localização**: Acesso via GPS ou entrada manual de coordenadas
- **🌤️ Dados Climáticos**: Informações meteorológicas em tempo real via OpenWeather API
- **📅 Previsão do Tempo**: Previsão de 5 dias para planejamento agrícola
- **📊 Dados Históricos**: Análise climática mensal via Meteostat API
- **🛰️ Análise por Satélite**: Imagens de satélite e análise de saúde das plantas
- **🤖 IA Integrada**: Análise inteligente para detecção de pragas e doenças
- **💡 Recomendações**: Sugestões personalizadas baseadas nos dados coletados

## 🛠️ Tecnologias Utilizadas

- **Next.js 15** - Framework React
- **TypeScript** - Tipagem estática
- **Tailwind CSS** - Estilização
- **Shadcn/UI** - Componentes de interface
- **OpenWeather API** - Dados meteorológicos
- **Meteostat API** - Dados climáticos históricos via RapidAPI
- **OpenRouter API** - Análise de IA

## 📋 Pré-requisitos

- Node.js 18+ 
- npm ou yarn
- Chaves de API (veja configuração abaixo)

## ⚙️ Configuração

### 1. Clone o repositório
```bash
git clone <repository-url>
cd agrohive
```

### 2. Instale as dependências
```bash
npm install
```

### 3. Configure as variáveis de ambiente

Copie o arquivo `.env.local.example` para `.env.local`:
```bash
cp .env.local.example .env.local
```

Edite o arquivo `.env.local` e adicione suas chaves de API:

```env
# OpenWeather API (OBRIGATÓRIA)
NEXT_PUBLIC_OPENWEATHER_API_KEY=sua_chave_openweather_aqui

# OpenRouter API (OBRIGATÓRIA)
NEXT_PUBLIC_OPENROUTER_API_KEY=sua_chave_openrouter_aqui

# Meteostat API via RapidAPI (OBRIGATÓRIA)
NEXT_PUBLIC_METEOSTAT_API_KEY=sua_chave_meteostat_aqui
NEXT_PUBLIC_RAPIDAPI_HOST=meteostat.p.rapidapi.com
```

### 4. Obtenha as chaves de API

#### OpenWeather API (Gratuita)
1. Acesse: https://openweathermap.org/api
2. Crie uma conta gratuita
3. Gere sua chave de API
4. Adicione no arquivo `.env.local`

#### OpenRouter API
1. Acesse: https://openrouter.ai/
2. Crie uma conta
3. Gere sua chave de API
4. Adicione no arquivo `.env.local`

#### Meteostat API (via RapidAPI)
1. Acesse: https://rapidapi.com/meteostat/api/meteostat
2. Crie uma conta no RapidAPI
3. Assine o plano gratuito da Meteostat API
4. Copie sua chave de API do RapidAPI
5. Adicione no arquivo `.env.local`

## 🚀 Executando o Projeto

### Modo de Desenvolvimento
```bash
npm run dev
```

O aplicativo estará disponível em: http://localhost:8000

### Build para Produção
```bash
npm run build
npm start
```

## 📱 Como Usar

### 1. **Configuração Inicial**
- Acesse a página inicial
- Permita acesso à localização ou insira coordenadas manualmente
- Clique em "Confirmar localização"

### 2. **Dashboard**
- Visualize dados climáticos em tempo real
- Consulte a previsão do tempo para os próximos dias
- Analise dados climáticos históricos mensais
- Receba insights agrícolas personalizados

### 3. **Análise por Satélite**
- Visualize imagens de satélite da sua propriedade
- Consulte análise de saúde das plantas
- Receba recomendações baseadas em IA

## 🏗️ Estrutura do Projeto

```
src/
├── app/                    # App Router (Next.js 13+)
│   ├── api/               # Rotas de API
│   │   └── meteostat/     # API do Meteostat
│   ├── dashboard/         # Dashboard principal
│   ├── satellite/         # Análise por satélite
│   ├── layout.tsx         # Layout global
│   └── page.tsx          # Página inicial
├── components/            # Componentes React
│   ├── ui/               # Componentes Shadcn/UI
│   ├── LocationInput.tsx # Componente de localização
│   └── MonthlyWeatherChart.tsx # Gráficos de dados mensais
├── context/              # Contextos React
│   └── LocationContext.tsx
├── lib/                  # Utilitários
│   ├── api.ts           # Funções de API
│   └── utils.ts         # Utilitários gerais
└── hooks/               # Hooks customizados
```

## 🔧 APIs Utilizadas

### Dados Meteorológicos
- **OpenWeather API**: Condições atuais e previsão do tempo
- **Meteostat API**: Dados climáticos históricos mensais via RapidAPI
- Endpoint: `https://meteostat.p.rapidapi.com/point/monthly`

### Análise por IA
- **OpenRouter API**: Análise de imagens de satélite
- Modelo: GPT-4o para análise agrícola
- Endpoint: `https://openrouter.ai/api/v1/chat/completions`

### Imagens de Satélite
- Integração com APIs de satélite (NASA/USGS)
- Análise de índices de vegetação (NDVI)

## 🎨 Design

O AgroHive utiliza um design moderno e minimalista com:
- **Cores**: Tons de verde (agricultura) com preto e branco
- **Tipografia**: Fontes Google Fonts para melhor legibilidade
- **Interface**: Clean e focada na funcionalidade
- **Responsivo**: Adaptado para desktop e mobile

## 🔒 Segurança

- Chaves de API armazenadas em variáveis de ambiente
- Validação de entrada de dados
- Tratamento de erros robusto
- HTTPS recomendado para produção

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Suporte

Para suporte e dúvidas:
- Abra uma issue no GitHub
- Entre em contato via email

---

**AgroHive** - Dados que cultivam o futuro 🌱
