---
layout: page
title: Mensagens - Documentação
permalink: /mensagens/
---
# Mensagens do sistema
O Message (Mensagem) é um Componente de Interface que tem como finalidade proporcionar feedback ao usuário sobre o que ocorre no sistema.

### Mensagem de texto fixa
Mensagem fixa no tipo da tela, especialmente utilizada para retorno de erro de preenchimento de dados em ficha de cadastro.

![image](https://github.com/robertobettega/Documentacao/assets/55776132/d2458756-65e7-435e-ab4f-4efeb7b08bb5)
 
    <div class="col-md-12">
                    <div class="alert alert-danger">
                        <p>
    •	O usuário deve possuir um ramal cadastrado em seu perfil    
                        <p>
                    </div>
    </div>

### Mensagem de pop-up
Mensagem de retorno de ação do sistema que surge como pop-up, centralizada na tela

![image](https://github.com/robertobettega/Documentacao/assets/55776132/837e72c3-c1f0-4fa5-9aa4-d73cf0a889dc) ![image](https://github.com/robertobettega/Documentacao/assets/55776132/2c2d7ab8-bfc3-4bb7-8c8f-b7b2391c81c6)

 
    function showSucess(title, text, subUrl) {
    var Sucess = {
        position: 'center',
        icon: 'success',
        title: title,
        text:text,
        showConfirmButton: false,
        timer: 2000,
        didOpen: () => {
            setTimeout(() => {
                window.location.replace(raizUrl + subUrl);
            }, 2000);
        }
    };
    addToQueue(Sucess);
    }
