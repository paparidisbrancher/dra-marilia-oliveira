# Site Dra. Marília Oliveira (em aprovação)

Site estático de uma página: `index.html` (CSS e JS embutidos), `assets/`, `fonts/`. Sem build, sem CDN e sem scripts externos.
Abra com qualquer servidor estático (ex.: `python -m http.server`).

Origem: protótipo `Site Dra Marilia Oliveira.dc.html` em `Downloads\marilia\` (briefing em `uploads/`), portado à mão para HTML estático por causa de SEO e prévia em redes sociais.

Demonstração: https://paparidisbrancher.github.io/dra-marilia-oliveira/ (GitHub Pages). Enquanto estiver em aprovação: `noindex` no `<head>` e `robots.txt` bloqueando buscadores.

## Pendências com a cliente

Nada não confirmado aparece no site. O que depende de confirmação ficou de fora ou em comentário no HTML.

- [ ] Nome completo e forma de apresentação
- [ ] Formação e qualificações; forma correta de divulgar a endodontia junto ao CRO-MG (o site diz "foco em endodontia", não "especialista")
- [ ] Endereço e mapa: uma publicação fixada cita Av. Governador Valadares, 787, Centro, Alpinópolis–MG (comentário na seção Contato)
- [ ] Clínica geral e facetas em resina: a seção "Outros atendimentos" está pronta, comentada no HTML
- [ ] Cidades atendidas, horários e condições da parceria com clínicas
- [ ] WhatsApp (35) 99862-4010 e Instagram @dra.mariliaoliveiracs (vieram da bio)
- [ ] Logo oficial (a assinatura em texto é provisória) e paleta (provisória, ver `:root`)
- [ ] Revisão clínica dos textos de Tratamento de canal, Como funciona e Perguntas frequentes, e da ilustração do dente em corte (legendas Esmalte, Dentina, Polpa e Canais)
- [ ] Publicidade conforme as normas do CFO e do CRO-MG
- [ ] Política de privacidade: só se entrar alguma ferramenta de análise ou rastreamento (hoje não há nenhuma)

## Imagens

Cada foto aparece uma vez só na página. As três são do ensaio corporativo de Jakeline Aguiar (@jakelineaguiarfoto_oficial), publicado em carrossel no Instagram em 04/06/2026 (8 fotos, 1365×1820).

| Arquivo | Foto do ensaio | Uso | Pendência |
|---|---|---|---|
| `ensaio-720/1100.webp` | blazer caramelo, banquinho | Início | Autorização da doutora e da fotógrafa |
| `sobre-700.webp` | terno escuro, encostada na parede, olhando para a câmera (recorte) | Sobre, em moldura de arco | Idem |
| `dentistas-600/900.webp` | blazer azul-marinho, braços cruzados (recorte 4:5) | Para dentistas | Idem |
| `og.jpg` | montagem com a foto do início | Compartilhamento | Idem |

Ainda não usadas: blazer marrom com luz lateral, duas de blusa branca no pedestal, blazer azul-marinho sentada (fundo bege), terno escuro em pé. Arquivos vieram do Instagram; pedir os originais à fotógrafa.

## SEO

Feito: título e descrição com tratamento e cidade, `canonical`, Open Graph e cartão do X, JSON-LD `Dentist` só com dados da bio, `sitemap.xml`, ícones, um único `h1`.

Para publicar de verdade:
1. Domínio próprio: trocar a URL do GitHub Pages em `index.html` (canonical, og, JSON-LD), `robots.txt` e `sitemap.xml`.
2. Tirar o `noindex` e trocar `Disallow: /` por `Allow: /`.
3. Google Search Console + sitemap. Ao confirmar o endereço, acrescentar `address` ao JSON-LD e criar o Perfil da Empresa no Google com os mesmos dados (para "tratamento de canal Alpinópolis" é ele que mais pesa).

## Design

- Títulos: Cormorant Garamond. Texto: Manrope. Assinatura cursiva (só na seção Sobre): Mrs Saint Delafield. Todas OFL, em `fonts/`.
- Diferenças em relação ao protótipo: sem a palavra em itálico colorida nos títulos, sem numeração "(01)…(06)" nas seções e sem rótulos em caixa alta. Numeração só onde há etapas de fato (Como funciona e os passos de Para dentistas); os tópicos de Tratamento de canal não têm marcador.
- Tratamento de canal tem uma ilustração própria (SVG no `index.html`) de um molar em corte, com a polpa e os canais em caramelo. Desenhada à mão, sem banco de imagens.
- Movimento: abertura no topo; a frase do Sobre ganha cor linha a linha ao rolar (CSS `animation-timeline: view()`; sem suporte, aparece pronta); o retrato sobe dentro do arco e o dente se desenha uma vez ao entrar na tela. Tudo desligado com "reduzir movimento".
- FAQ com `<details>` nativo e menu do celular com `<dialog>` nativo (foco preso, Esc fecha). Botão flutuante do WhatsApp só no celular, depois do topo.

## Referências premiadas (consultadas em 01/11/2026)

Sites de clínicas odontológicas premiados no Awwwards. Serviram de princípio, nada foi copiado.

| Site | Prêmio | O que aproveitamos |
|---|---|---|
| [Aventura Dental Arts](https://aventuradentalarts.com/) | Site do Dia, mar/2026 | Frase de apresentação em serifa grande que ganha cor ao rolar; retrato pequeno junto do texto |
| [Dębski Clinic](https://www.debskiclinic.pl) | Menção honrosa, out/2023 | Retrato da médica em moldura de arco; tom pessoal e acolhedor |
| [LAVA dental](https://lavadental.lv/en) | Menção honrosa, jan/2026 | Contenção: poucas cores, movimento discreto, clareza em vez de apelo de venda |
| [Minemal Dental Aesthetics](https://minemal.dental/) | Menção honrosa, nov/2024 | A tipografia como protagonista; o próprio dente como tema visual |

O Cabinet Dentaire Gonin Hetzel (menção honrosa, 2021) ficou de fora: o domínio expirou e hoje mostra outro site.
