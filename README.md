# Sistema de Monitoramento de Temperatura e Umidade

Sistema multiplataforma para monitoramento em tempo real de dados de temperatura e umidade, composto por backend Node.js, frontend React.js e aplicativo mobile para Android e iOS.

## Arquitetura do Sistema

O projeto é dividido em três componentes principais:

- **Backend (Node.js)**: API REST com WebSocket para comunicação em tempo real
- **Frontend (React.js)**: Interface web responsiva para visualização dos dados
- **Mobile (Android/iOS)**: Aplicativo nativo para dispositivos móveis

## Tecnologias Utilizadas

### Backend

- Node.js com Express
- Firebase/Firestore para persistência de dados
- WebSocket para comunicação em tempo real
- CORS para requisições cross-origin
- Moment.js para manipulação de datas

### Frontend

- React.js 18
- Axios para requisições HTTP
- CSS customizado para estilização
- WebSocket client para atualizações em tempo real
- Componentes de loading e histórico

### Mobile

- Suporte para Android e iOS
- Interface nativa para cada plataforma
- Consumo da API REST
- Componentes de design nativos

## Funcionalidades

### Backend

- Endpoint para listar dados meteorológicos
- Endpoint para adicionar novos dados de sensores
- Busca filtrada por data e hora
- Comunicação WebSocket para atualizações em tempo real
- Integração com Firebase para armazenamento

### Frontend

- Visualização em tempo real de temperatura e umidade
- Ícones dinâmicos baseados nas condições climáticas
- Histórico de medições com busca por data/hora
- Interface responsiva e intuitiva
- Atualizações automáticas via WebSocket

### Mobile

- Visualização de dados meteorológicos
- Lista histórica de medições
- Interface nativa para Android e iOS

## Estrutura do Projeto

```
Temperatura-Multiplataforma--JS/
├── Back-end--NodeJs/          # API Node.js
│   ├── src/
│   │   ├── firebase/          # Configuração Firebase
│   │   ├── app.js            # Servidor principal
│   │   └── app-ws.js         # Configuração WebSocket
│   └── package.json
├── Front-end--ReactJs/        # Aplicação React
│   ├── src/
│   │   ├── components/       # Componentes React
│   │   ├── img/             # Ícones e imagens
│   │   └── App.js           # Componente principal
│   └── package.json
└── Mobile--Kotlin/           # App Mobile
    ├── app/src/main/java/
    │   └── com/example/weatherviewapi/
    │       ├── UI/          # Activities
    │       ├── Adapter/     # RecyclerView adapters
    │       ├── Domains/     # Modelos de dados
    │       └── Network/     # Serviços de rede
    └── build.gradle.kts
```

## Instalação e Execução

### Backend

```bash
cd Back-end--NodeJs
npm install
npm start
```

Servidor rodará na porta 3004

### Frontend

```bash
cd Front-end--ReactJs
npm install
npm start
```

Aplicação rodará na porta 3000

### Mobile

1. Abra o projeto no Android Studio
2. Sincronize as dependências Gradle
3. Execute no emulador ou dispositivo físico

## Configuração

### Variáveis de Ambiente (Backend)

Crie um arquivo `.env` no diretório do backend:

```
PORT=3004
CORS_ORIGIN=*
```

### Firebase

Configure as credenciais do Firebase no arquivo `src/firebase/index.js`

## API Endpoints

- `GET /` - Página inicial da API
- `GET /listWeather` - Lista todos os dados meteorológicos
- `GET /buscar?date=&hour=` - Busca por data e hora específicas
- `POST /addWeather` - Adiciona novos dados do sensor
- `WebSocket ws://localhost:3004` - Comunicação em tempo real

## Autores

| Nome                     | LinkedIn                                                  | Responsabilidade                          |
| ------------------------ | --------------------------------------------------------- | ----------------------------------------- |
| Nayara Nasaria Soares    | [LinkedIn](https://www.linkedin.com/in/nayaranasaria/)    | API e Front-end Web                       |
| Laisla Stephanie Barbosa | [LinkedIn](https://www.linkedin.com/in/laisla-stephanie/) | Mobile                                    |
| Rafael Alcântara França  | [LinkedIn](https://www.linkedin.com/in/rafaelalfr/)       | Integração API, Mobile e Front-end ao ESP |

## Licença

ISC License

---

Desenvolvido para a aula de Desenvolvimento Multiplataforma - Fatec Zona Leste

---
© 2024 - Sistema de Monitoramento de Temperatura e Umidade
