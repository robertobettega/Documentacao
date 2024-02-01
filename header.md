---
layout: page
title: Header - Documentação
permalink: /header/
---

# Cabeçalho

O componente Header é o principal elemento de uma página, onde podem ser agrupados componentes predefinidos que tem como finalidade auxiliar o usuário no acesso ou mesmo execução das funcionalidades principais site/sistema.

Por padrão, todos os sistemas exibem a logo do tribunal no canto superior esquerdo. Na linha abaixo, segue como primeira opção o nome do sistema (clicável como botão para tela inicial), e em seguida as opções de navegação entre as telas do sistema.

Para melhor entendimento da estrutura da página e agilidade no desenvolvimento de novos sistemas, está anexo a este documento arquivo de toda a página de layout padrão utilizado no tribunal (extraída do sistema DSG Online).

[Página de layout padrão](_Layout.cshtml)

 ![image](https://github.com/robertobettega/Documentacao/assets/55776132/d572db0b-b61c-4c60-98cf-a10c93bef21e)

    <header style="margin-bottom: 20px;">
        <nav class="navbar navbar-expand-sm navbar-toggleable-sm navbar navbar-light" id="navPrincipal">
            <div class="container">
                <environment include="Development">
                    <a class="navbar-brand" asp-controller="Home" asp-action="Index">
                        <img class="img-fluid" src="~/Imagens/logo_tcmrio2.png" />
                    </a>
                </environment>
                <environment include="Staging">
                    <a class="navbar-brand" asp-controller="Home" asp-action="Index" style="color: darkgreen;">HOMOLOGAÇÃO
                        <img class="img-fluid" src="~/Imagens/logo_tcmrio2.png" />
                    </a>
                </environment>
                <environment include="Production,Contingencia">
                    <a class="navbar-brand" asp-controller="Home" asp-action="Index">
                        <img class="img-fluid" src="~/Imagens/logo_tcmrio2.png" />
                    </a>
                </environment>
                <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#collapsibleNavbarPrincipal">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="collapsibleNavbarPrincipal">
                    <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                        @if (User.Identity.IsAuthenticated)
                        {
                            <li class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle btn" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">                                    
                                    @User.GetUserName().Split(' ')[0]                                  
                                </a>
                                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                                    <li>
                                        <a asp-controller="Home" asp-action="LogOut" class="dropdown-item">Sair</a>
                                    </li>
                                </ul>
                            </li>
                        }
                    </ul>
                </div>
            </div>
        </nav>
        <nav class="navbar navbar-expand-sm border-bottom navbar-light" id="subnavAtos">
            <div class="container">
                <a class="navbar-brand">
                    @{
                        string label = @ConfiguracoesService.ChamadoUrl == "ChamadoDSG" ? "DSGOnline" : "STI Online";
                    }
                    @label
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavbar">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="collapsibleNavbar">
                    <ul class="navbar-nav">
                        <li class="nav-item dropdown">
                            @{
                                string activeClass = ViewData["Title"]?.ToString() == "Abrir Chamado" ? "fade show active" : "";
                            }
                            <a class="nav-link @activeClass" asp-area="" asp-controller="@ConfiguracoesService.ChamadoUrl" asp-action="AbrirChamado">Abrir Chamado</a>
                        </li>
                    </ul>
                    <ul class="navbar-nav">
                        <li class="nav-item dropdown">
                            @{
                                activeClass = ViewData["Title"]?.ToString() == "Central de Notificação" ? "fade show active" : "";
                            }
                            <a class="nav-link @activeClass" asp-area="" asp-controller="Notificacao" asp-action="Index">Central de Notificação <span class="badge badge-danger badge_notificacoes"></span></a>
                        </li>
                    </ul>
                    <ul class="navbar-nav">
                        <li class="nav-item dropdown">
                            @{
                                activeClass = ViewData["Title"]?.ToString() == "Chamado" ? "fade show active" : "";
                            }
                            <a class="nav-link @activeClass" asp-area="" asp-controller="@ConfiguracoesService.ChamadoUrl" asp-action="Index">Histórico de Chamados</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>                
    </header>
