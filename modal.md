---
layout: page
title: Mmodal - Documentação
permalink: /modal/
---

# Modal
Modal é uma janela que exibe um conteúdo adicional em uma camada acima da página atual, com uma sobreposição de superfície (overlay) cobrindo a página e tornando-a temporariamente inacessível.

### Modal informativo
Utilizado como área de exibição de mensagem. Sem ação extra necessária.

 ![image](https://github.com/robertobettega/Documentacao/assets/55776132/a3f88b54-ae7a-4685-90cf-c1e6cb46d4b1)

    <div class="row">
    <div class="modal fade" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
    <div class="modal-header">
    <h4 class="modal-title fs-5" Ver nota</h4>
    </div>
    <div class="modal-body">
    <div class="mb-3">
    <label for="recipient-name" class="col-form-label">Mensagem:</label>
                                            <p>@n.TextoDaNotificacao</p>
                                        </div>
                                        <div class="modal-footer">
                                            <form value="Fechar">
                                                <input type="submit" class="btn btn-secondary" value="Fechar" />
                                            </form>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

### Modal com input
Modal para inserção de nova mensagem do usuário. Quando se faz necessário um novo campo de texto sem precisar atualizar a tela.
   
![image](https://github.com/robertobettega/Documentacao/assets/55776132/26765f7c-d2c2-4217-b1d5-8139e3bc7d41) ![image](https://github.com/robertobettega/Documentacao/assets/55776132/28e3e32d-eaca-45ea-a724-cb6a33f4d8c2)


(Exemplo do código do modal “Nova nota)

    <div class="card-header d-flex general-title col-12 align-items-center">
    <h4 class="flex-grow-1" id="titulo-listagem">Notas</h4>
    <a class="btn btn-outline-primary" data-bs-toggle="modal" data-bs-target="#InserirNotaModal" title="Nova nota">
        <i class="bi bi-plus" aria-hidden="true"></i>
    </a>
    </div>
    <div id="tabela-notas" class="col-12 table-notes">
    <div class="row">
        <div class="col">
            <div id="table-notes">
                <div class="col-12">
                    <table id="tabela_notas" class="display responsive wrap table table-striped">
                        <thead>
                            <tr>
                                <th>Mensagem</th>
                                <th>Envio</th>
                                <th>Remetente</th>
                                <th>Destinatário</th>
                                <th>Detalhes</th>
                            </tr>
                        </thead>
                        <tbody>
                            @if (Model.NotificacoesOrderByDateDesc != null)
                            {
                                @foreach (var notificacao in Model.NotificacoesOrderByDateDesc)
                                {
                                    <tr class="table-tr">
                                        <td>@notificacao.TextoDaNotificacao</td>
                                        <td>@notificacao.GetDataEnvioSemSegundos()</td>
                                        @if (notificacao.Remetente != null)
                                        {
                                            <td>@notificacao.Remetente.Name</td>
                                        }
                                        else
                                        {
                                            <td>[ChamadosOnline]</td>
                                        }

                                        @if (notificacao.Destinatario != null)
                                        {
                                            <td>@notificacao.Destinatario.Name</td>
                                        }
                                        else
                                        {
                                            <td>[ChamadosOnline]</td>
                                        }
                                        <td>
                                            <a class="btn-primary" data-bs-toggle="modal" data-bs-target="#DetalhesModal_@notificacao.Id" title="Ver Notificação">
                                                <i class="bi bi-search" aria-hidden="true"></i>
                                            </a>
                                        </td>

                                    </tr>

                                }
                            }
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
    </div>
