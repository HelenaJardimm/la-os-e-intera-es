# la-os-e-intera-es

HTML

1. **Estrutura HTML básica**:
   - O documento começa com a declaração `&lt;!DOCTYPE html&gt;` e a tag `&lt;html&gt;`.
   - O `&lt;head&gt;` inclui informações de metadados, como o conjunto de caracteres (`&lt;meta charset='utf-8'&gt;`), a compatibilidade com diferentes versões do IE (`&lt;meta http-equiv='X-UA-Compatible' content='IE=edge'&gt;`), o título da página (`&lt;title&gt;Page Title</title&gt;`), e a configuração de viewport (`&lt;meta name='viewport' content='width=device-width, initial-scale=1'&gt;`).
   - Também há links para uma folha de estilo CSS externa (`&lt;link rel='stylesheet' type='text/css' media='screen' href='Laço.css'&gt;`) e um script JavaScript (`&lt;script src='main.js'&gt;&lt;/script&gt;`).
 
2. **Corpo do Documento (`&lt;body&gt;`)**:
   - Dentro do `&lt;body&gt;`, há um formulário (`&lt;form name="selectForm"&gt;`) com:
     - Um parágrafo (`&lt;p&gt;`) contendo um rótulo (`&lt;label&gt;`) e uma lista suspensa (`&lt;select&gt;`). A lista suspensa (`&lt;select id="tipoMusica" name="tipoMusica" multiple="multiple"&gt;`) permite múltiplas seleções e contém várias opções de tipos de música, com "R&B" selecionado por padrão.
     - Um parágrafo com um botão (`&lt;p&gt;&lt;input id="btn" type="button" value="Quantos foram selecionados?" /&gt;&lt;/p&gt;`).
 
3. **Script JavaScript embutido**:
   - A função `howMany(selectObject)` percorre todas as opções da lista suspensa e conta quantas estão selecionadas. Ela retorna o número de opções selecionadas.
   - Um evento é adicionado ao botão (`btn.addEventListener("click", function () {...})`). Quando o botão é clicado, ele executa uma função que exibe um alerta com o total de opções selecionadas, chamando a função `howMany(document.selectForm.tipoMusica)` e passando a lista suspensa como argumento.
 
**Resumo do funcionamento**:
- O usuário pode selecionar múltiplas opções da lista de tipos de música.
- Ao clicar no botão "Quantos foram selecionados?", um alerta é exibido mostrando quantas opções foram selecionadas.
 
Esse código combina HTML para a estrutura da página, CSS (referenciado externamente) para o estilo, e JavaScript para a interação e manipulação dinâmica do conteúdo.

CSS

Estilização Global:*, *::before, *::after {
    box-sizing: border-box;
}Define box-sizing: border-box para todos os elementos e seus pseudo-elementos ::before e ::after, garantindo que o padding e a borda sejam incluídos na largura e altura dos elementos.Variáveis CSS::root {
    --select-border: #12d792;
    --select-focus: rgb(8, 8, 8);
    --select-arrow: var(--select-border);
}Define variáveis CSS (--select-border, --select-focus, --select-arrow) para facilitar a reutilização de valores de cores ao longo do estilo.Estilização do <select>:select {
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background-color: rgb(245, 245, 245);
    border: greenyellow;
    padding: 0 1em 0 0;
    margin: 0;
    width: 100%;
    font-family: inherit;
    font-size: inherit;
    cursor: inherit;
    line-height: inherit;