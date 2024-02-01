---
layout: page
title: Paginação
permalink: /paginacao/
---
# Paginação
O Pagination é um componente de interface que tem a função de organizar conteúdo de dados em páginas sequenciais, trazendo maior usabilidade durante o consumo da informação pelo usuário.
EXIGE DATATABLE

### Paginação padrão
 
![image](https://github.com/robertobettega/Documentacao/assets/55776132/fa816b15-c055-4eb9-87b7-85c3447e0009)<br>
![image](https://github.com/robertobettega/Documentacao/assets/55776132/0513a368-9e3b-4170-9a41-4d0ccf4facec)


    $(an).each(function(index,item) {
            var $item = $(item);
           
            if (oPaging.iPage == 0) {
                var prev = $item.find('span.paginate_button.first').add($item.find('span.paginate_button.previous'));
                prev.addClass("disabled");
            }else {
                var prev = $item.find('span.paginate_button.first').add($item.find('span.paginate_button.previous'));
                prev.removeClass("disabled");
            }
    }

