# inemaseo-sistemas

[![inemaseo-sistemas](guia/assets/banner.jpg)](https://inematds.github.io/inemaseo-sistemas/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

O inemaseo-sistemas Ã© um conjunto de cinco programas gratuitos para cuidar do SEO (como o site aparece no Google e nas IAs) do **seu prÃ³prio** site. Serve para quem tem um site e quer saber o que estÃ¡ quebrado, quem te encontra, quais robÃ´s de IA leem as pÃ¡ginas e se o site estÃ¡ pronto para agentes de IA. Tudo roda no seu computador, com o Python 3.10 ou mais novo, usando sÃ³ dado grÃ¡tis: o site, o log do servidor e os arquivos que o Search Console e o Bing Webmaster deixam baixar.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/inemaseo-sistemas/guia/**

ðŸŽ¬ VÃ­deo: https://www.youtube.com/watch?v=R5jHoJJzi4I

O "Semrush aberto" do **seu prÃ³prio site**: 5 ferramentas de linha de comando que rodam no seu computador, sÃ³ com Python 3.10+ (biblioteca padrÃ£o), sem API paga e sem conta em serviÃ§o nenhum alÃ©m do Search Console e do Bing Webmaster, que sÃ£o grÃ¡tis. LicenÃ§a MIT.

Faz parte do [inemaSEO](https://eventos.inema.pro/inemaseo/) e Ã© a base do curso 7 da FormaÃ§Ã£o inemaSEO.

| ferramenta | o que responde | de onde vem o dado |
|---|---|---|
| [gsc-historico](ferramentas/gsc-historico/) | quantas buscas **sem a sua marca** te acharam, semana a semana, para sempre (o Search Console sÃ³ guarda 16 meses) | CSV do `gsc_semanal.py` (Search Console) |
| [bing-ia](ferramentas/bing-ia/) | quais pÃ¡ginas o Copilot/Bing citou e se elas tambÃ©m tÃªm clique no Google | export do Bing Webmaster AI Performance |
| [botlog](ferramentas/botlog/) | quais robÃ´s de IA leram o site de verdade, por finalidade (busca, pedido do usuÃ¡rio, treino), e quais sÃ£o falsos | log de acesso do seu servidor + listas oficiais de IP |
| [auditor](ferramentas/auditor/) | o que estÃ¡ quebrado no HTML que o servidor entrega (canÃ´nico, hreflang, sitemap, robots por finalidade, bloqueio de CDN, Ã³rfÃ£s) | o seu site, rastreado com educaÃ§Ã£o |
| [agente-ready](ferramentas/agente-ready/) | nota 0â€“100 de prontidÃ£o para IA e agentes, com pesos pÃºblicos | o seu site |

## ComeÃ§ar
```bash
git clone https://github.com/inematds/inemaseo-sistemas && cd inemaseo-sistemas
python3 ferramentas/auditor/auditor.py https://seusite.com --max 50
python3 ferramentas/agente-ready/agente-ready.py https://seusite.com
```
Cada pasta tem o prÃ³prio README com todos os comandos, o limite honesto da ferramenta e as fontes. Exemplos reais (sites do INEMA, 19/10/2026) em [exemplos/](exemplos/).

## O que dÃ¡ e o que nÃ£o dÃ¡ para fazer de graÃ§a
DÃ¡: auditoria tÃ©cnica, histÃ³rico do Search Console, citaÃ§Ãµes oficiais do Bing, robÃ´s de IA no log, nota de prontidÃ£o. **NÃ£o dÃ¡** sem dado pago: volume exato de busca, dificuldade de palavra-chave, SERP de concorrente, backlinks completos e monitor automÃ¡tico das respostas das IAs. Para isso existem DataForSEO, Firecrawl, Apify, Semrush e Ahrefs â€” opcionais, fora deste repo. Comparativo em [docs/ESPEC.md](docs/ESPEC.md).

## Testes
```bash
for t in ferramentas/*/; do [ -d $t/tests ] && python3 -m unittest discover -s $t/tests; done
```

---
**English:** [README.en.md](README.en.md) Â· guide: https://inematds.github.io/inemaseo-sistemas/guia/en/
**EspaÃ±ol:** [README.es.md](README.es.md) Â· guÃ­a: https://inematds.github.io/inemaseo-sistemas/guia/es/

---

Projeto adaptado da comunidade INEMA TDS - Marca Arckhe