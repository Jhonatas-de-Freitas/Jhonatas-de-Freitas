# Jhonatas de Freitas

Desenvolvedor de Software Full Stack. Trabalho com back-end em Java e Spring Boot e faço o front em React e TypeScript.

Gosto de entender como as partes de um sistema conversam: filas, eventos, o que acontece quando um serviço cai no meio do caminho. Os projetos abaixo são um sistema de pedidos que montei para estudar e mostrar isso na prática, do banco até a tela.

Tenho 25 anos e curso Análise e Desenvolvimento de Sistemas na PUC-RS e Tecnologia da Informação na UFMS.

## Projetos

Os cinco repositórios formam um sistema só. Cada um roda sozinho com `docker compose up`, e todos têm testes rodando no GitHub Actions.

| Projeto | O que é | Tecnologias |
|---|---|---|
| [order-platform](https://github.com/Jhonatas-de-Freitas/order-platform) | Três microsserviços (pedidos, estoque e pagamento) que conversam por eventos. Saga coreografada, outbox transacional, consumidor idempotente e fila de erros. | Java 21, Spring Boot, Kafka, PostgreSQL |
| [api-gateway](https://github.com/Jhonatas-de-Freitas/api-gateway) | Porta de entrada do sistema: login com JWT, limite de requisições por usuário e circuit breaker. | Spring Cloud Gateway, Keycloak, Redis, Resilience4j |
| [notification-service](https://github.com/Jhonatas-de-Freitas/notification-service) | Notificações por e-mail, SMS e push, com fila por canal, novas tentativas e agendamento. | Java 21, Spring Boot, RabbitMQ, PostgreSQL |
| [order-dashboard](https://github.com/Jhonatas-de-Freitas/order-dashboard) | Painel para acompanhar os pedidos em tempo real. Tem um modo de demonstração que roda direto no navegador. | React, TypeScript, Vite, Tailwind |
| [order-analytics](https://github.com/Jhonatas-de-Freitas/order-analytics) | Lê os eventos do Kafka e transforma em números: faturamento, cancelamentos, produtos mais vendidos. | Python, FastAPI, PostgreSQL |

Para ver funcionando sem instalar nada: [demonstração do painel](https://jhonatas-de-freitas.github.io/order-dashboard/).

```mermaid
flowchart LR
    painel[order-dashboard] --> gateway[api-gateway]
    gateway --> plataforma[order-platform]
    gateway --> notificacoes[notification-service]
    gateway --> metricas[order-analytics]
    plataforma -- eventos no Kafka --> notificacoes
    plataforma -- eventos no Kafka --> metricas
```

## Tecnologias

<p>
  <img alt="Java" title="Java" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" />
  <img alt="Spring" title="Spring Boot" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg" />
  <img alt="Kafka" title="Apache Kafka" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/apachekafka/apachekafka-original.svg" />
  <img alt="RabbitMQ" title="RabbitMQ" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/rabbitmq/rabbitmq-original.svg" />
  <img alt="PostgreSQL" title="PostgreSQL" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg" />
  <img alt="Redis" title="Redis" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg" />
  <img alt="Docker" title="Docker" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg" />
  <img alt="TypeScript" title="TypeScript" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" />
  <img alt="React" title="React" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" />
  <img alt="Python" title="Python" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" />
  <img alt="FastAPI" title="FastAPI" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/fastapi/fastapi-original.svg" />
  <img alt="Git" title="Git" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" />
  <img alt="GitHub Actions" title="GitHub Actions" width="36" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/githubactions/githubactions-original.svg" />
</p>

Também uso no dia a dia: Next.js, Node.js, Supabase, Vercel, Prometheus e Grafana.

## Contato

- LinkedIn: [jhonatas-de-freitas](https://www.linkedin.com/in/jhonatas-de-freitas-1276a321b)
- E-mail: jhonatas.freitas@icloud.com
