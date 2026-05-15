# Maquina Viral Scheduler

Este repositorio publico guarda apenas o robo externo do Maquina Viral.

Ele nao contem codigo do sistema nem tokens visiveis. Os segredos ficam salvos em GitHub Actions Secrets:

- `CRON_URL_TOKEN`: autoriza chamada no Maquina Viral.
- `WORKFLOW_PAT`: permite o workflow iniciar o proximo ciclo automaticamente.

O workflow chama a agenda varias vezes por ciclo e, ao terminar, dispara a proxima execucao sozinho.

Endpoint chamado:

```text
https://maquina-viral.vercel.app/api/schedule/run?limit=10
```