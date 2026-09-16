# Maquina Viral Scheduler

Este repositorio publico guarda apenas o robo externo do Maquina Viral.

Ele nao contem codigo do sistema nem tokens visiveis. O segredo fica salvo em GitHub Actions Secrets:

- `CRON_URL_TOKEN`: autoriza a chamada no Maquina Viral.

## Como funciona

O GitHub Actions chama a agenda do Maquina Viral a cada 5 minutos.

Endpoint chamado:

```text
https://maquina-viral.vercel.app/api/schedule/run?limit=10
```

O workflow tambem pode ser iniciado manualmente pela aba **Actions** usando `workflow_dispatch`.

## Importante sobre repositorios publicos

O GitHub pode desativar automaticamente workflows agendados em repositorios publicos apos 60 dias sem atividade no repositorio. Alterar o cron ou reativar o workflow pela aba Actions volta a habilitar o agendamento.

Para uma segunda camada de redundancia, o projeto tambem documenta o uso do cron-job.org como plano B.
