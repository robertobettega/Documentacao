---
layout: page
title: "Input - Documentação"
permalink: /input/
---
# Input
Componente que permite a entrada de dados textuais por parte do usuário.

### Input padrão

![image](https://github.com/robertobettega/Documentacao/assets/55776132/376db78f-8db1-4c3d-84ea-c6325c7f67c3)
 
    <label><b>Ramais:</b></label><label style="color:red"> *</label>
    <input class="form-control telefone" maxlength="16"/>

### Input com seletor

![image](https://github.com/robertobettega/Documentacao/assets/55776132/e7e04b1b-ac3a-49f5-971e-c289fb07d7a4)
 
            <select class="form-select">
                <option value="0" disabled selected>Selecione um assunto</option>
            </select>

### Input desativado

![image](https://github.com/robertobettega/Documentacao/assets/55776132/4a1b3f05-c90f-4543-b7db-ac432e6ec6e2)

 
      <label asp-for="Chamado.UsuarioAbertura"><b>Matrícula:</b></label>
      <input class="form-control" value=“810014 Roberto Bettega Medeiros Peixoto” disabled />
