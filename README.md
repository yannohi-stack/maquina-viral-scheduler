# Maquina Viral Scheduler

Este repositorio publico guarda apenas o robo externo do Maquina Viral.

Ele nao contem codigo do sistema nem tokens visiveis. O segredo fica salvo em GitHub Actions Secrets como `CRON_URL_TOKEN`.

A cada 5 minutos o workflow chama:

```text
https://maquina-viral.vercel.app/api/schedule/run?limit=10
```