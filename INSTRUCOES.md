# Como publicar o README

## 1. Estrutura

O repositório **`icaroiene/icaroiene`** (que já existe) precisa ficar assim:

```
icaroiene/
├── README.md                      ← o perfil
└── .github/
    └── workflows/
        └── snake.yml              ← gera a animação da snake
```

Suba os dois arquivos na branch `main`.

## 2. Ativar a Snake Animation

A seção 07 só aparece depois que o workflow rodar pelo menos uma vez.

1. Suba `.github/workflows/snake.yml`.
2. Vá em **Actions** no repositório → aceite habilitar workflows, se pedir.
3. Abra **Generate Snake Animation** → **Run workflow** → `main` → **Run workflow**.
4. Espere ~1 minuto. O job cria a branch `output` com `github-snake.svg` e `github-snake-dark.svg`.
5. Recarregue o perfil — a snake aparece.

Depois disso ele roda sozinho a cada 6 horas.

> Se der erro de permissão, vá em **Settings → Actions → General → Workflow permissions** e marque **Read and write permissions**.

## 3. Contato

O badge de e-mail na seção 08 aponta para `icaroienexd@gmail.com`. Para trocar depois, é só editar o `mailto:` — ou apagar o bloco `<a>...</a>` inteiro, que o badge some e os outros continuam alinhados.

## 4. Sobre os cards de estatística

As instâncias oficiais desses dois serviços **estão fora do ar**:

| Serviço | Host oficial | Status hoje |
| :--- | :--- | :--- |
| GitHub Readme Stats | `github-readme-stats.vercel.app` | `503 DEPLOYMENT_PAUSED` |
| GitHub Profile Trophy | `github-profile-trophy.vercel.app` | `402 DEPLOYMENT_DISABLED` |

O README usa espelhos públicos que estão funcionando:

- `gh-readme-stats.vercel.app` — stats, top languages e os 3 repo cards
- `github-trophies.vercel.app` — troféus

Espelho é deploy de terceiro: pode cair ou mudar sem aviso. **Recomendo fazer o seu próprio** — leva uns 5 minutos e aí nada quebra:

1. Faça fork de <https://github.com/anuraghazra/github-readme-stats>.
2. Em <https://vercel.com>, importe o fork e faça deploy (plano gratuito serve).
3. Crie um GitHub Personal Access Token (classic, sem escopo nenhum) e cadastre como variável de ambiente `PAT_1` no projeto da Vercel.
4. Você recebe um domínio tipo `https://seu-projeto.vercel.app`.
5. No README, substitua todas as ocorrências de `gh-readme-stats.vercel.app` por esse domínio.

Mesma receita para os troféus, com fork de <https://github.com/ryo-ma/github-profile-trophy> (esse não precisa de token).

Os demais serviços usados são estáveis e não precisam de nada:
`shields.io`, `skillicons.dev`, `readme-typing-svg.demolab.com`, `streak-stats.demolab.com`, `capsule-render.vercel.app`, `github-readme-activity-graph.vercel.app`, `komarev.com`.

## 5. Paleta usada

Herdada do seu site, em versão dark:

| Token | Hex | Onde aparece |
| :--- | :--- | :--- |
| Background | `#0A0A0A` | base do banner |
| Surface | `#0D0D0F` | fundo dos cards e badges |
| Hairline | `#1F1F23` | bordas dos cards |
| Texto | `#F5F5F7` | texto principal |
| Muted | `#86868B` | texto secundário |
| Accent | `#0A84FF` | títulos, links, destaques |
| Glow | `#64D2FF` | ícones, pontos, terminal |

Para mudar o acento, troque `0A84FF` e `64D2FF` em todo o arquivo.

## 6. Manutenção

Os cards de repositório da seção 04 apontam para `pizzaria_do_leo`, `grafos-p2p-gnutella` e `hash-linear-avaliacao`; ao criar repositórios novos, é só trocar o `repo=` na URL. Todo o resto (stats, linguagens, streak, gráfico de atividade, troféus) se atualiza sozinho — não precisa mexer.

As seções são: `01` Sobre mim · `02` Tech stack · `03` Ferramentas · `04` Projetos · `05` GitHub stats · `06` Conquistas · `07` Snake · `08` Conecte-se.
