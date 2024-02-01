---
layout: page
title: Cards - Documentação
permalink: https://robertobettega.github.io/Documentacao/cards/
---


# Card

Cards são cartões ou superfícies que contém conteúdo resumido acerca de um assunto. Ele é clicável e deve direcionar o usuário a tela onda a informação está contida por completo.

### Card de resumo numérico
Traz uma informação que pode ser resumida a um número. Geralmente uma estatística sobre o sistema.

![image](https://github.com/robertobettega/Documentacao/assets/55776132/fae5e40c-fe6e-452e-b61d-05a97626e2fa)

    <a style="text-decoration: none;" class="card card-called red card-visual">
        <div class="card-content">
            <div class="card-body">
                <div>
                    <div class="media-body text-center" style="min-height: 101.98px">
                        <h3 class="badge bg-primary rounded-pill">10</h3>
                        <h5>Chamados abertos do órgão</h5>
                    </div>
                </div>
            </div>
        </div>
    </a>

### Card de resumo com texto
Traz uma informação com conteúdo de texto resumido. Aplicado idealmente a sistemas com abertura de chamados.

![image](https://github.com/robertobettega/Documentacao/assets/55776132/686018f2-c6a6-4962-b8b1-02ddfc093555)

   	  <div class="col-sm-6 col-md-6 col-lg-4">
                        <div class="card bg-white p-3 mb-4 shadow">
                            <div class="d-flex justify-content-between mb-4">
                                <div class="user-info">
                                    <div class="user-info__basic">
                                        <h5 class="mb-0">Chamado 124-2024</h5>
                                        <p class="text-muted mb-0">Categoria: Bombas</p>
                                    </div>
                                </div>
                            </div>
                            <div>
                                <h6 class="mb-0">Data de abertura: 23/01/2024 13:58</h6>
                                <div class="d-flex justify-content-between mt-4">
                                    <div>
                                        <h5 class="mb-0">
                                            Status:
                                            <small class="ml-1">Aberto</small>
                                        </h5>
                                    </div>
                                    <div>
                                        <a title="Ver chamado">
                                            <i class="bi bi-search" aria-hidden="true"></i>
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

### Card de corpo de página

![image](https://github.com/robertobettega/Documentacao/assets/55776132/c4d53ca4-fa4d-4fe8-8966-51424d628757)
 
    <div class="card border-0">
      <div class="card-header">
         <h5 class="font-weight-bold mb-0">Abrir Chamado</h5>
      </div> 
    </div> 
