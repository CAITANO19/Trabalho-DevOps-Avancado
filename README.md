# Trabalho DevOps Avançado: GitHub Actions

Coleção de 12 workflows de **GitHub Actions** que exploram diferentes gatilhos e automações de CI: execução manual, em eventos de push, filtros por caminho de arquivo e agendamento com `cron`.

## Workflows

| # | Workflow | Gatilho |
| --- | --- | --- |
| 01 | Hello World | Manual e alteração do próprio arquivo |
| 02 | Informações do push (data/hora e usuário) | Push na `main`, ignorando `.github/workflows/**` |
| 03 | Calcular 2+2 | Manual |
| 04 | Listar arquivos | Manual e push |
| 05 | Contar arquivos HTML | Manual e push que altere `*.html` |
| 06 | Criar README automático | Manual |
| 07 | Rodar apenas à noite (horário de São Paulo) | Agendado (`cron`) e manual |
| 08 | Rodar apenas aos sábados (horário de São Paulo) | Agendado (`cron`) e manual |
| 09 | Alerta de arquivos maiores que 100 KB | Push na `main` e manual |
| 10 | Estatísticas do push (em sequência) | Push na `main` |
| 11 | Estatísticas do push (em um único step) | Push na `main` |
| 12 | Contar arquivos à meia-noite (São Paulo) | Agendado (`cron`) e manual |

Os workflows 10 e 11 fazem o mesmo trabalho de duas formas (vários steps e um único step), para comparar as abordagens.

## Conceitos praticados

- Gatilhos `push`, `workflow_dispatch` e `schedule`
- Filtros `paths` e `paths-ignore`
- Conversão de fuso horário em expressões `cron` (UTC para São Paulo)
- Scripts shell dentro de steps
- Organização de steps e jobs

## Como usar

1. Faça um fork ou clone do repositório.
2. Abra a aba **Actions** no GitHub.
3. Execute os workflows com gatilho manual em **Run workflow**, ou faça um push para disparar os demais.

Os arquivos `index.html`, `style.css` e `app.js` servem de conteúdo para os workflows que contam e listam arquivos.

## Autor

Victor Caitano — [@CAITANO19](https://github.com/CAITANO19)
