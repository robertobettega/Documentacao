---
layout: page
title: Tags- Documentação
permalink: /tags/
---

# Tag
Tag é qualquer tipo de sinalizador que pode indicar um status, uma quantidade ou uma informação de forma precisa e direta.

### Tag de contagem (notificação)
Esta tag pode ser utilizada como contador de notificações do sistema, ou como alerta para nova mensagem interna. Utilizado geralmente em contexto de card, mas pode ser utilizado em outro contexto.

![image](https://github.com/robertobettega/Documentacao/assets/55776132/28329ea5-d842-48da-9330-0280b66cd8f6)

 HTML

    <li class="nav-item dropdown">
    <a class="nav-link" asp-action="Index">Central de Notificação <span class="badge badge-danger badge_notificacoes"></span></a>
    </li>

CSS

    .badge_notificacoes {
    background-color: red;
    color: #fff;
    }

Tag de texto
Utilizado para dar realce a um texto informativo.

![image](https://github.com/robertobettega/Documentacao/assets/55776132/8d5d09ef-a2cf-4f2b-865f-95d4ad10d642)

<div>
          <span class="badge bg-success fs-14 mt-1">126/2024</span>
          <span class="badge bg-soft-secondary fs-14 mt 1">23/01/2124 23:59</span>
</div>
