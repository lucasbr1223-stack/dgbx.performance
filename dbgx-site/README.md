# DBGX Performance: site da loja

Site estático de uma página (HTML, CSS e JavaScript em um único arquivo). Não precisa de servidor nem de banco de dados.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub, por exemplo `dbgx-performance`. Pode ser público.
2. Envie os arquivos desta pasta (`index.html`, `.nojekyll` e `README.md`) para a raiz do repositório.
   Pelo site do GitHub, use **Add file > Upload files** e arraste os arquivos.
3. Vá em **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`. Clique em **Save**.
5. Em um a dois minutos, o site fica disponível em `https://SEU-USUARIO.github.io/dbgx-performance/`.

Para usar um domínio próprio (ex.: dbgxperformance.com.br), configure em **Settings > Pages > Custom domain** e aponte o DNS conforme a documentação do GitHub.

## Como atualizar

Todos os dados ficam no início do bloco `<script>` do `index.html`:

- **Número do WhatsApp:** constante `WHATSAPP` (atualmente 5519982855723).
- **Produtos:** lista `PRODUTOS`. Para colocar um preço, troque `preco: null` pelo valor, por exemplo `preco: 189.90`. Enquanto estiver `null`, o site mostra "Consulte o preço".
- **Imagens:** as fotos estão embutidas no próprio arquivo, dentro de `IMG`. Para trocar uma foto, substitua o conteúdo da chave correspondente por uma imagem em base64 ou por um arquivo na mesma pasta (ex.: `"whey": "fotos/whey.jpg"`).
- **Horários:** a função `atualizarStatus` tem os horários de funcionamento. Ajuste ali se mudarem.

Depois de editar, faça o upload do `index.html` de novo. O GitHub Pages atualiza em poucos minutos.

## Observações

- Os preços e as informações de produtos devem ser confirmados com a loja antes de publicar.
- Suplementos não substituem alimentação. O rodapé já traz esse aviso.
