# Robson Silva — presença digital

Página única de elétrica e hidráulica, feita para transformar visitas em conversas no WhatsApp. Estética preto e dourado, tipografia serifada e foco total no celular.

## Arquivos

| Arquivo | Para que serve |
| --- | --- |
| `index.html` | Site completo (HTML, CSS e JS no mesmo arquivo, sem build) |
| `assets/og.png` | Cartão 1200 × 630 exibido quando o link é compartilhado no WhatsApp |
| `assets/favicon.svg` | Ícone da aba do navegador |
| `og.html` | Fonte do cartão social, caso queira editar e gerar a imagem de novo |
| `README.md` | Este guia |

## Ver agora

Dê dois cliques em `index.html`. As fontes vêm do Google Fonts, então é preciso estar conectado à internet. Não há instalação, servidor ou banco de dados.

## Site publicado

- **Página:** <https://vtrpza.github.io/robson-silva/>
- **Repositório:** <https://github.com/vtrpza/robson-silva>
- **Sitemap:** <https://vtrpza.github.io/robson-silva/sitemap.xml>
- **Atualizações:** todo `push` na branch `main` republica o site em cerca de 1 minuto.

## Revisar antes de divulgar (5 minutos)

1. **Confirme a região:** o site diz “Campinas e região” em vários pontos. Se o atendimento for outra cidade, use Localizar e Substituir por “Sua Cidade e região”.
2. **Confira o telefone:** o número aparece como `(19) 98356-4986` (visível) e `5519983564986` (links). Troque os dois formatos em todo o arquivo se necessário.
3. **Ajuste o que for combinado com o Robson:** o site não promete preço, prazo, garantia, horário de atendimento nem formas de pagamento. Se quiser incluir, acrescente apenas informações confirmadas.
4. **Não invente avaliações ou números.** A página foi escrita sem depoimentos falsos; a confiança vem do atendimento real.

## Como atualizar

### GitHub Pages (publicação atual)

1. Edite `index.html` (ou os textos do README).
2. No terminal, dentro da pasta:
   ```bash
   git add .
   git commit -m "Atualiza o site"
   git push
   ```
3. O GitHub Pages detecta o push e publica sozinho. Acompanhe em **Settings → Pages** ou na aba **Actions**.
4. Para trocar a imagem de compartilhamento, substitua `assets/og.png` mantendo 1200 × 630 px.

### Netlify Drop (alternativa)

1. Acesse <https://app.netlify.com/drop>.
2. Arraste a pasta inteira (`robs`) para a página.
3. Em **Site configuration → Change site name**, troque para algo como `robson-silva-eletrica`.

### Imagem de compartilhamento e SEO

O `og:image`, o `twitter:image`, o JSON-LD e o canônico já apontam para `https://vtrpza.github.io/robson-silva/`. Se um dia usar domínio próprio, troque esses endereços no `<head>` do `index.html`:

```html
<meta property="og:image" content="https://SEU-DOMINIO.com/assets/og.png">
<meta name="twitter:image" content="https://SEU-DOMINIO.com/assets/og.png">
<link rel="canonical" href="https://SEU-DOMINIO.com/">
```

E o campo `"url"` e `"image"` do JSON-LD. O WhatsApp exige URL absoluta para exibir a prévia. Teste em <https://www.opengraph.xyz/> ou enviando o link para você mesmo.

Depois de qualquer mudança, abra o site no celular e toque em **Falar no WhatsApp** para confirmar que a conversa abre com a mensagem pronta.

## O combo de validação digital

O site sozinho não sustenta a presença. A sequência que funciona é esta:

### 1. WhatsApp Business (o centro do atendimento)

- Instale o **WhatsApp Business** e confirme o número.
- Nome do perfil: `Robson Silva — Elétrica e Hidráulica`
- Categoria: `Serviço de reformas` ou `Eletricista`
- Foto: use a mesma identidade do site (fundo escuro, monograma ou foto do Robson).
- Descrição (copie e cole):

  > Elétrica, hidráulica e pequenos reparos em Campinas e região. Tomadas, chuveiros, torneiras, vazamentos, desentupimento e mais. Orçamento sem compromisso pelo WhatsApp.

- Cadastre os serviços no **catálogo** (sem preço, se preferir): Elétrica, Hidráulica, Pequenos reparos.
- Crie **respostas rápidas**:

  **Saudação**
  > Olá! Você está falando com o Robson, de elétrica e hidráulica. Me conte o que precisa e, se puder, envie uma foto do local. Assim já consigo te passar um orçamento.

  **Orçamento**
  > Para eu te passar o valor certo, me confirma: 1) o que está acontecendo; 2) seu bairro; 3) se prefere manhã ou tarde. Se tiver foto, ajuda bastante.

- Use **etiquetas** simples: `Orçamento`, `Agendado`, `Concluído`, `Avaliação pedida`.
- Configure uma **mensagem de ausência** para horários sem atendimento, sem prometer resposta imediata.

### 2. Perfil da Empresa no Google (para ser encontrado)

1. Acesse <https://business.google.com> e crie o perfil.
2. Categoria principal: **Eletricista**; secundária: **Encanador**.
3. Se atende em domicílio, escolha **área de atendimento** (Campinas e cidades vizinhas) em vez de exibir endereço.
4. Cole o link do site publicado e o mesmo telefone do WhatsApp.
5. Adicione fotos reais de serviços (antes/depois, ferramentas, atendimento).
6. Peça avaliações aos primeiros clientes. Link direto: no painel do perfil, **Pedir avaliações**.
7. Mantenha nome, telefone e cidade iguais no site, no Google e no Instagram.

### 3. Instagram e cartão

- Bio sugerida:
  > Elétrica e hidráulica ⚡🔧
  > Pequenos reparos com capricho
  > Campinas e região
  > Orçamento no WhatsApp ↓
- Coloque o link do site na bio.
- No cartão de visita ou panfleto, use um QR Code apontando para o site. O botão **Compartilhar** no rodapé também facilita o envio do link.
- O botão **Salvar contato** baixa um arquivo `.vcf` com nome, telefone e serviços — útil para o cliente guardar o contato.

### 4. Pedido de avaliação (copie e cole)

> Oi, [nome]! Que bom que o serviço ficou bem feito. Se puder, me deixe uma avaliação no Google? Ajuda muito o meu trabalho a aparecer para outras pessoas. Segue o link: [link da avaliação]

## Checklist de lançamento

- [ ] Telefone e região conferidos
- [ ] Site publicado e link aberto no celular
- [ ] Botão do WhatsApp testado (mensagem abre preenchida)
- [ ] `og:image` com URL absoluta e prévia testada
- [ ] WhatsApp Business com foto, descrição, catálogo e respostas rápidas
- [ ] Perfil da Empresa no Google criado e verificado
- [ ] Link do site na bio do Instagram
- [ ] 3 a 5 fotos reais de serviços separadas para o Google e o site
- [ ] Primeiros clientes convidados a avaliar
- [ ] Revisar o texto a cada 3 meses (serviços, região, fotos)

## Observações técnicas

- **Sem backend:** o formulário de orçamento apenas monta uma mensagem e abre o `wa.me`. Nenhum dado é armazenado, o que simplifica a LGPD.
- **Sem rastreadores:** não há cookies, pixels ou analytics instalados.
- **Acessibilidade:** navegação por teclado, link “pular para o conteúdo”, foco visível e respeito a `prefers-reduced-motion`.
- **SEO local:** título, descrição, Open Graph e dados estruturados `LocalBusiness` já estão no arquivo. Atualize a cidade se o atendimento mudar e as imagens se criar um domínio próprio.
- **Manutenção:** todo o visual está no topo do `index.html`, nas variáveis CSS. O telefone e a mensagem automática do formulário ficam no final do arquivo, no bloco de script (`WA_NUMBER`).
