# Site Dra. Marília Oliveira (em aprovação)

Site estático de uma página: `index.html` (CSS e JS embutidos), `assets/`, `fonts/`. Sem build, sem CDN e sem scripts externos.
Abra com qualquer servidor estático (ex.: `python -m http.server`).

Origem: protótipo `Site Dra Marilia Oliveira.dc.html` em `Downloads\marilia\` (briefing em `uploads/`), portado à mão para HTML estático por causa de SEO e prévia em redes sociais.

URL prevista: https://paparidisbrancher.github.io/dra-marilia-oliveira/ (ainda não publicado). Enquanto estiver em aprovação: `noindex` no `<head>` e `robots.txt` bloqueando buscadores.

## Pendências com a cliente

Nada não confirmado aparece no site. O que depende de confirmação ficou de fora ou em comentário no HTML.

- [ ] Nome completo e forma de apresentação
- [ ] Formação e qualificações; forma correta de divulgar a endodontia junto ao CRO-MG (o site diz "foco em endodontia", não "especialista")
- [ ] Endereço e mapa: uma publicação fixada cita Av. Governador Valadares, 787, Centro, Alpinópolis–MG (comentário na seção Contato)
- [ ] Clínica geral e facetas em resina: a seção "Outros atendimentos" está pronta, comentada no HTML
- [ ] Cidades atendidas, horários e condições da parceria com clínicas
- [ ] WhatsApp (35) 99862-4010 e Instagram @dra.mariliaoliveiracs (vieram da bio)
- [ ] Logo oficial (a assinatura em texto é provisória) e paleta (provisória, ver `:root`)
- [ ] Revisão clínica dos textos de Tratamento de canal, Como funciona e Perguntas frequentes
- [ ] Publicidade conforme as normas do CFO e do CRO-MG
- [ ] Política de privacidade: só se entrar alguma ferramenta de análise ou rastreamento (hoje não há nenhuma)

## Imagens

| Arquivo | Origem | Uso | Pendência |
|---|---|---|---|
| `ensaio-720/1100.webp` | `marilia-ensaio.jpg` (ensaio de estúdio) | Início | Autorização da doutora e da fotógrafa; pedir original |
| `detalhe-600.webp` | recorte do mesmo ensaio | Sobre | Idem |
| `retrato-350.webp` | recorte da publicação de apresentação do Instagram, sem os textos | Para dentistas | Baixa resolução (350 px); pedir foto original |
| `og.jpg` | montagem com o ensaio | Compartilhamento | Idem ao ensaio |

## SEO

Feito: título e descrição com tratamento e cidade, `canonical`, Open Graph e cartão do X, JSON-LD `Dentist` só com dados da bio, `sitemap.xml`, ícones, um único `h1`.

Para publicar de verdade:
1. Domínio próprio: trocar a URL do GitHub Pages em `index.html` (canonical, og, JSON-LD), `robots.txt` e `sitemap.xml`.
2. Tirar o `noindex` e trocar `Disallow: /` por `Allow: /`.
3. Google Search Console + sitemap. Ao confirmar o endereço, acrescentar `address` ao JSON-LD e criar o Perfil da Empresa no Google com os mesmos dados (para "tratamento de canal Alpinópolis" é ele que mais pesa).

## Design

- Títulos: Cormorant Garamond. Texto: Manrope. Assinatura cursiva (só na seção Sobre): Mrs Saint Delafield. Todas OFL, em `fonts/`.
- Diferenças em relação ao protótipo: sem a palavra em itálico colorida nos títulos, sem numeração "(01)…(06)" nas seções e sem rótulos em caixa alta. A numeração ficou só onde há etapas de fato. Uma única animação de abertura no topo, que respeita "reduzir movimento".
- FAQ com `<details>` nativo e menu do celular com `<dialog>` nativo (foco preso, Esc fecha). Botão flutuante do WhatsApp só no celular, depois do topo.
