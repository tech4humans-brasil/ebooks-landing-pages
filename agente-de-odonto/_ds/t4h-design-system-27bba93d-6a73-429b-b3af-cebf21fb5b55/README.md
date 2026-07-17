# T4H — Tech for Humans · Design System

Design system for **Tech for Humans (T4H)** — uma consultoria estratégica de IA brasileira que une estratégia + execução para grandes operações (Porto, Allianz, Mapfre, Caixa, CNP, Magalu, Sisprime…). Lançou em 2025 sua linha de Agentes de IA, copilotos inteligentes que substituem chatbots tradicionais. Sede em São Paulo.

> **Posicionamento:** "Desenhamos jornadas digitais e Agentes de IA que transformam complexidade tecnológica em experiências verdadeiramente humanas."
> **Arquétipo:** Sábia / Parceira — fala como quem já sabe o caminho e caminha junto.
> **Tom:** Tecnológico · Moderno · Amigável.

---

## Index — manifest of this folder

| Path | Purpose |
|---|---|
| `colors_and_type.css` | Foundational CSS variables — color, type, spacing, radii, shadows, motion. Plus `.t4h-display`, `.t4h-h1`, `.t4h-body`, `.t4h-eyebrow` semantic classes. |
| `fonts/` | Inter Light / Regular / SemiBold (TTF). **Bold + ExtraBold not supplied** — see Caveats. |
| `assets/` | Logos (full + glyph), client logos, gradient PNGs, "raios" backgrounds, humano-IA hero image. |
| `assets/clients/` | All client logos (Porto, Allianz, Mapfre, Caixa, CNP, Magalu, Sisprime, Unifisa, Tradição, Facil-Assist, Canopus, Evorab, Porto-Seguro-Bank). |
| `preview/` | 21 preview cards consumed by the Design System tab. |
| `slides/` | 5-slide sample deck (cover, metrics, manifesto, pillars, clients) using `deck-stage.js`. |
| `ui_kits/marketing/` | Full marketing-site recreation — `index.html`, `components.jsx`, `styles.css`, `README.md`. |
| `SKILL.md` | Cross-compatible skill manifest for use in Claude Code. |

---

## Sources

All design context was extracted from two design-token JSONs supplied at project start:
- `t4h-design-tokens.json` — extracted from Instagram / LinkedIn posts (March–April 2026)
- `t4h-design-tokens-apresentacoes.json` — extracted from "Apresentação Institucional T4H" + "Proposta Executiva Sisprime"

Plus 30+ visual assets: full logo + glyph (PNG/SVG, light + dark), 12 client logos, 3 fonts (Inter), 8 background gradients, 3 "raios" wave backgrounds, the humano-IA hero photo, a building photo, transparent overlay versions.

> **No production codebase or Figma file was provided.** UI kits are recreated from the social posts and the two presentations described in the token JSONs. If you have the Figma source for `Apresentação Institucional T4H` or the marketing-site repo, sharing it would let us tighten pixel parity.

---

## Content Fundamentals

### Voice
Three modifiers, in order of weight: **Tecnológico · Moderno · Amigável.**

- **Tecnológico, sem exibicionismo.** Use a linguagem do setor com precisão. "Agente", "fábrica de IA", "human-in-the-loop", "FCR", "retenção". Nunca "soluções inovadoras de ponta", nunca "transformação digital".
- **Moderno = frases curtas + ritmo ágil.** Sem orações encadeadas. Sem jargão corporativo. Quando uma frase puder virar duas, vire duas.
- **Amigável = par inteligente.** Trate o leitor como executivo que entende do próprio negócio. Nunca explique o óbvio, nunca faça micro-pergunta retórica ("Já parou para pensar como…?").

### Pessoa & casing
- **Você**, sempre. Nunca "vocês", nunca "nós, da T4H, acreditamos que…".
- Sentence case em títulos. ALL-CAPS apenas em labels de eyebrow / metadata (≤16 chars).
- "Agente" e "Agentes de IA" capitalizados quando se referem ao produto. "T4H" sempre em caixa-alta sem ponto.

### Frases-modelo
- **Headline-padrão (manifesto):** *"Humanos e Agentes, lado a lado."*
- **Posicionamento:** *"Tecnologia que potencializa pessoas."*
- **Diferencial:** *"Estratégia com execução. Sem jargão."*
- **Resultado:** *"Agentes que resolvem, não apenas respondem."*
- **CTA:** *"Falar com a T4H →"* / *"Marcar conversa →"*. Nunca "Saiba mais", "Clique aqui", "Entre em contato hoje mesmo".

### Não-fazer
- ❌ Emoji em copy institucional. Nunca.
- ❌ Exclamações. Period.
- ❌ Hashtags em peças que não sejam social.
- ❌ Listas com "✓" ou "🚀". Use border-left bars verdes.
- ❌ "Soluções de ponta", "estado da arte", "líder no segmento", "best-in-class".

### Destaques inline
Palavras-chave dentro do corpo aparecem em **verde** (`#48BA80`) — uma a duas por bloco. Em peças "Trends" usa-se **teal** (`#56C4C0`) no lugar.

---

## Visual Foundations

### Color
Two-temperature system: **dark navy + green/teal accents** (institutional, posts, slides escuros) e **off-white + corner-bleed mint** (propostas, slides claros).

- **Primary brand green:** `#48BA80` — CTAs, keywords, border-left bars, badges. (Source-of-truth do Figma — supera o `#48BA80` que aparecia nos tokens JSON anteriores.)
- **Primary dark surface:** `#131C23` — most posts, all dark slides. `#051721` é o tom mais frio usado em capas.
- **Vibrant teal:** `#1AB19E` — núcleo dos gradientes mesh; também o fundo do metric card primário (`#19B99C`).
- **Off-white paper:** `#F8F9FA` — slides de proposta. Sempre acompanhado de **corner-bleed mint** (`#9CC2C0`) no canto superior esquerdo.

Veja `colors_and_type.css` para a lista completa (greens 400–700, teals 200–600, ink 300–900, mints 50–400, paper 50–white).

### Type
**Inter** como família única. Pesos usados: Light (300, atmospheric), Regular (400, body), SemiBold (600, UI/títulos), Bold (700, headlines), ExtraBold (800, métricas e display de capa). Letterforms com `feature-settings: "ss01", "cv11"` — single-storey *a*, *g* simplificado.

Escala (presentations 1920×1080):
`metric 80 / display 56 / heading 36 / subheading 22 / body 16 / caption 14 / meta 13`.
Escala (social 1080×1080): `display 64 / heading 40 / subheading 28 / body 20 / label 16`.

Letter-spacing apertado em headlines (−2%); padrão em corpo; +4% em eyebrows; +8% em meta uppercase.

### Spacing
Grid de 4 px. Escala-chave: `4 · 8 · 12 · 16 · 24 · 32 · 40 · 48 · 56 · 80`. Padding de slide: 80 H × 56 V. Padding de post (1080²): 48 todos os lados. Gaps típicos: 16 (cards), 32 (sections em social), 40 (sections em presentations), 48 (column gap).

### Backgrounds
Quatro famílias, todas em PNG (em `assets/`):

1. **Gradientes "padrão"** — abstratos, blurry, lisos. Usados full-bleed em slides hero e covers. Variantes: escuro, claro, cor (verde→teal→navy), branco, black, padrão-cor.
2. **"Raios"** — wave-light streaks (verde nasceu da esquerda, ondula para a direita). Variantes: verde, escuro, claro. Renderizam em `mix-blend-mode: screen` sobre fundos sólidos.
3. **Mesh-cover** — gradient mesh multi-radial (verde + teal + navy) gerado via 3 `radial-gradient` sobrepostos. Capa institucional.
4. **Imagery** — `bg-humano-ia.png` (rosto humano + cabeça circuit-board) e `bg-edificio.png` (arranha-céu noturno). Aplicadas com scrim escuro `linear-gradient(180deg, rgba(5,23,33,.2), rgba(5,23,33,.85))`.

### Borders & corner radii
- `4 · 8 · 12 · 16 · 999` px.
- Pills (999) para CTAs, badges, eyebrow-pills.
- Cards = 16 px. Containers = 12 px. Tags = 4 px.
- Border-width: hairline 1, thin 1.5 (CTAs e outlined cards), bar 4 (substitui bullets).

### Border-left bar system
**Não usamos bullet points.** Em listas e callouts, blocos de texto recebem uma `border-left: 4px` colorida + 2px de raio:
- **Verde claro `#48BA80`** = pilar positivo, ponto estratégico, valor.
- **Verde escuro `#06625A`** = ponto de atenção, problema, contexto crítico.
- **Callout box translúcido** = `rgba(72,186,128,.18)` com `border-left: 2px #48BA80` e raio 12 px.

### Shadows & elevation
Marca **flat-first** — confia em gradiente de fundo + cor para hierarquia, não em shadow. Quando elevamos:
- `shadow/sm` — resting (1 px sutil).
- `shadow/md` — cards interativos.
- `shadow/lg` — modals e overlays.
- `glow/teal` — `0 0 40px rgba(26,177,158,.45)` — apenas em CTAs primary sobre fundo escuro, ou em chip ativo.

### Imagery vibe
**Cool / cinematic / verde-teal washed.** Fotos sempre passam por overlay teal-escuro (rgba 11,27,38,.55). Pessoas iluminadas de baixo, tom esmeralda. Edifícios em ângulo low-angle, vidro espelhado refletindo o céu noturno teal. Nada de stock vibrante, nada de warm/grãos. Quando a foto não estiver disponível, usar `bg-humano-IA.png` ou `bg-edificio.png`.

### Animation
- **Easing padrão:** `cubic-bezier(.2,.6,.2,1)` (standard) e `cubic-bezier(.2,.8,.2,1)` (emphasized).
- **Durações:** fast 150 / normal 240 / slow 420 ms.
- **Hover:** transição de cor + leve `translateY(-2px)` em cards interativos. Nunca scale.
- **Press:** `translateY(1px)`. Sem mudança de cor adicional.
- **Sem bounces, sem confetti.** A marca é confiante e contida — animação serve a navegação, não a celebração.

### Hover & press states
- **Botão primary:** verde 400 → verde 500 (`#48BA80` → `#239A78`).
- **Botão outline-light:** transparente → `rgba(72,186,128,.08)`.
- **Botão outline-dark:** transparente → `rgba(255,255,255,.08)`.
- **Link nav:** `rgba(255,255,255,.78)` → `#fff`.
- **Card interativo:** background levemente mais opaco + `translateY(-2px)`.

### Layout rules (slides)
- **Logo top-left** sempre que o slide for escuro. **Logo bottom-right (em preto)** quando o slide for claro/proposta.
- **Breadcrumb top-center** (`Contexto | Subcontexto`) em slides institucionais.
- **Header bar** com `N/ Nome da seção ———— Documento · Data` em slides de proposta (light theme).
- **Page number bottom-right** em meta uppercase, formato `01 / 05`.
- **Section transition** = full-bleed gradient `divider` (teal vibrante → verde profundo → navy) com texto centralizado.

### Transparency & blur
- **Backdrop blur 16 px** em sticky navs (`rgba(19,28,35,.65)`).
- **Modal scrim** `rgba(5,23,33,.6)` + blur 8 px.
- **Glass surfaces** (cards sobre dark hero): `rgba(255,255,255,.04)` + border `rgba(255,255,255,.08)`. Hover sobe para `.07` + border-accent verde.

### Cards
- Conteúdo: `bg #fff` (sobre dark) ou `bg rgba(255,255,255,.04)` (em dark theme), raio 16, padding 20–24, gap 16, header opcional, sem shadow por padrão.
- Métrica: raio 16, padding 28–32, layout `num à esquerda · label à direita`. Variantes verde-vibrante / mint / teal-dark.
- Outlined diagrama: border 1.5 px verde, transparente, raio 12, hover sobe opacidade do fill verde a 12%.

---

## Iconography

T4H **não usa um icon font ou sistema de ícones próprio nas peças fornecidas.** As apresentações e posts dependem de:

1. **O glyph "T4H"** (em `assets/icon-black.svg` / `icon-white.svg`) como mark único. É um pictograma único e não-decomponível — não há "ícone de chat" ou "ícone de chave" derivados.
2. **Border-left bars** no lugar de ícones de bullet.
3. **Numeração** (`01 ·` `02 ·` …) em verde como marcador visual em vez de ícones temáticos.
4. **Setas inline (→)** como CTA marker — tipográficas, não SVGs. Render via `<span aria-hidden>→</span>`.

**Sem emoji em peça institucional. Sem unicode-icons (✓, ★, etc).** A única "estrela" tolerada (★) é o marcador editorial de "primary brand color" nos preview cards deste design system.

**Ação para iconografia futura.** Quando icons forem necessários (ex.: features grid, settings UI de um produto), recomendamos **Lucide** (`https://unpkg.com/lucide@latest/dist/umd/lucide.min.js`) — stroke 1.5, geometric, casa com Inter. Sinalize a substituição na hora de usar e peça ao cliente para validar.

---

## Caveats — peça ao usuário

- ✅ **Inter Bold + ExtraBold** agora carregados em `fonts/`. Headlines e métricas renderizam no peso correto.
- ✅ **Figma de apresentações** consumido — slides reconstruídos com os layouts reais (cover, green-mesh quote, section intro, metrics, pillars, light proposal, split, 2x2, clients, CTA). O verde primário foi promovido para `#48BA80` para casar com a Figma (141 referências).
- ✅ **PDFs institucional + Sisprime** anexados — assumimos que os layouts já refletem a linguagem dos PDFs; valide e nos diga se há slide-tipo faltando.
- ⚠️ **O codebase do site `techforhumans.com.br`** ainda não foi importado. O UI kit em `ui_kits/marketing/` é uma recriação a partir do tokens + assets. Para pixel-parity, importe o repo via Import → Codebase.
- ⚠️ **Linha de produto "Agentes de IA"** (a UI do copilot que vai dentro de Porto/Allianz) não está representada — não há código nem screenshots dela. Se houver um console do agente, vale criar um segundo UI kit `ui_kits/agente/`.
