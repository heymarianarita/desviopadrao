# Desvio Padrão — Plano do site

**Estado:** site construído. Este documento descreve o que existe e o que falta.
**Ficheiros:** pasta `site/`. Abre-se o `index.html` num browser, sem servidor nem build.
**Peso:** 1,6 MB, dos quais 946 KB de fotografias e 150 KB de tipos de letra.

---

## 0. Dados confirmados

| Assunto | Valor |
|---|---|
| Morada | R. Amélia Rey Colaço, n.º 38, Carnaxide |
| Horário | Segunda a sexta, 10:00–12:30 e 14:00–19:00 |
| Modalidades | No centro, online e ao domicílio (Lisboa) |
| Formato | Individual |
| Níveis | 1.º ciclo ao ensino superior |
| Disciplinas | Todas |
| Nomenclatura | **Explicações**, não "aulas" |
| Primeira explicação | Uma **apresentação**: o aluno e o explicador conhecem-se, falam sobre o que está a correr mal e definem os passos seguintes |
| Compra de horas | Avulso, ou um pack de 4 horas com desconto — o único que existe |
| Preçário | **Não publicado.** Valores enviados a pedido |
| Inscrição | Ficha em PDF; a maioria envia os dados por WhatsApp e o centro preenche |
| Contactos | geral@desviopadrao.pt · 214 100 902 · 964 989 883 |

**32 marcadores POR PREENCHER** no site, em cinzento neutro. Lista na secção 9.

---

## 1. Princípio editorial

O site não argumenta. Descreve.

Sem campanhas nem tráfego pago, quem chega já foi recomendado. Não precisa de ser
convencido de que explicações servem para alguma coisa; precisa de saber **o que se faz,
se serve para o caso, e como se inscreve.**

- Sem posicionamento nem promessas. Nada de "método único" ou "excelência".
- Sem comparações com concorrentes.
- Sem agitação emocional.
- Sem slogans. Títulos que informam.
- Factos concretos em vez de adjetivos.
- **Nada de afirmações não confirmadas.** Em particular, o site nunca diz que a primeira
  explicação é gratuita — isso nunca foi confirmado. Diz o que ela é.

---

## 2. Tratamento do leitor

Três registos. É uma regra de manutenção: quem mexer no copy tem de saber em que
registo está.

| Páginas | Registo | Exemplo |
|---|---|---|
| `alunos.html` | **tu** | "A explicação é só tua, e trabalha o que precisas de trabalhar." |
| `pais.html` | **formal, 3.ª pessoa** | "A explicação anda ao ritmo do seu filho." · "Se achar que não está a resultar, pode pedir para mudar de explicador." |
| todas as outras | **impessoal** | "Compra-se um pack de horas e marcam-se as explicações conforme a necessidade." |

**Porque é que as páginas partilhadas são impessoais.** A homepage, `como-funciona`,
`disciplinas`, `sobre`, `contactos` e `inscricao` são lidas pelas duas audiências, e a
bifurcação só acontece a meio da homepage. Não podem tratar por "tu" quem vai ser
tratado formalmente duas páginas depois.

**Sobre "você".** O `pais.html` é formal mas não usa a palavra "você", que em Portugal
soa brusca por escrito. Usa verbo na 3.ª pessoa mais "o seu".

**"Encarregado de educação", não "pais".** É o termo em toda a navegação, no cartão de
bifurcação e nos títulos. Inclui avós e tutores, que "pais" exclui. Dentro do texto usa-se
"o seu filho", que é o caso real de quase todos. O URL continua `pais.html`, porque mudar
endereços custa mais do que vale.

---

## 3. Estrutura

```
index.html            Homepage — bifurcação encarregados/alunos
├── pais.html         1.º ciclo ao 9.º ano · registo formal
├── alunos.html       Secundário + ensino superior · registo "tu"
├── como-funciona.html  Modalidades, a primeira explicação, formato, horas
├── disciplinas.html  Lista por nível
├── sobre.html        Centro, equipa, espaço
├── contactos.html    Morada, mapa, WhatsApp, pedido de valores
└── inscricao.html    Ficha em PDF ou envio de dados por WhatsApp

assets/style.css      Toda a folha de estilos
assets/fonts/         Space Grotesk e Inter, variáveis, subset latino
assets/logo/          Logótipo oficial, quatro variantes
assets/fotos/         Fotografias do espaço, duas larguras cada
```

Oito páginas. **Menu:** Encarregados · Alunos · Como funciona · Disciplinas · Sobre ·
Contactos, mais o botão de Inscrição.

### O que saiu, e porquê

| Removido | Razão |
|---|---|
| `precos.html` | O preçário não é para divulgar. O modelo de compra é explicado, os valores pedem-se. |
| `marcar.html` | A inscrição não é um formulário web. Passou a `inscricao.html` e descreve o processo real. |
| Secções de testemunhos | Sem citações reais, um bloco de testemunhos denuncia-se. Markup guardado no LEIA-ME. |
| Páginas por disciplina | Sem marketing digital não compensam, e com "todas as disciplinas" seriam 25 páginas a desatualizar. |

---

## 4. A página de inscrição

É a página que mais se afasta do plano inicial, porque o processo real não é um formulário.

**Via 1 — ficha em PDF.** Descarregar, preencher, enviar por email ou entregar no centro.
O ficheiro ainda não existe, por isso o site diz isso e oferece pedir a ficha por email,
em vez de mostrar um botão que não faz nada.

**Via 2 — WhatsApp.** É o caminho que a maioria usa. O botão abre uma conversa com uma
mensagem já preenchida com a lista de campos, para só ser preciso escrever ao lado de
cada um. O centro depois transcreve para a ficha.

**Lista de dados** apresentada nas duas vias. Tem de corresponder exatamente aos campos
da ficha em PDF — está marcada como POR PREENCHER até isso ser confirmado.

Depois: confirma-se explicador → marca-se a primeira explicação → combinam-se as horas
e os valores.

> **Nota.** O PDF é atrito: obriga a descarregar, abrir, preencher e reenviar, e em
> telemóvel quase ninguém o faz — daí a maioria ir por WhatsApp. Se algum dia houver
> orçamento para um formulário web que gere o PDF preenchido, é o único investimento
> técnico deste site que se paga a si mesmo.

---

## 5. Identidade gráfica

Tokens do Manual de Normas Gráficas (agosto 2026), no topo de `style.css`: rampas
completas de navy, blue, orange e cinzas, nos sete tons.

**Tipografia auto-alojada.** Space Grotesk nos títulos e etiquetas, Inter no texto
corrido. Variáveis, subset latino: 31 KB e 118 KB em woff. Sem Google Fonts.

**Logótipo oficial** em `assets/logo/`, variante `primary-light-horizontal` sobre os
fundos escuros do header e do rodapé.

### Cor de ação: laranja

Botões em **laranja `#EF7639` — o do manual, sem alterações — com texto navy-70 e um
contorno navy de 1,5px**. O texto dá 6.38:1; o contorno resolve a fronteira sobre os
fundos claros, onde o laranja sozinho só separa 2.77:1. Sobre fundos escuros é o próprio
laranja que separa (4.85:1 no navy).

Sem anéis creme em volta dos botões. A fronteira vem do contorno navy, que é da mesma cor
do texto e por isso lê-se como parte do botão.

**O laranja não é fundo de secção.** Com botões laranja, um fundo laranja tornava-os
invisíveis, e qualquer texto sobre `#EF7639` obrigava a escolher entre falhar o contraste
(creme, 2.77:1) ou o aspeto de escuro-sobre-laranja. O laranja ficou reservado às ações.
Para não desaparecer do site, os **padrões de pontos** das secções escuras são laranja —
um padrão de pontos nunca se confunde com um botão.

**O amarelo não é usado.**

### Ritmo de cor: sem alternância mecânica

Alternar faixas de cor a cada secção lê-se como listas de pijama, e punha todas as
páginas com a mesma sequência. A cor entra de três maneiras:

1. **Faixas de largura total** — duas ou três por página, como pontuação.
2. **Painéis contidos** — `.panel`, `.panel.p-blue`, `.panel.p-navy`: blocos de cor com
   cantos arredondados dentro de secções claras. É assim que o azul e o navy aparecem a
   meio de uma página sem cortar o ecrã em bandas.
3. **Duas superfícies claras** — creme `#FFFBF0` e o branco do manual `#F9FAFB`,
   alternadas automaticamente pelo gerador, com uma linha fina a separá-las.

| Tom | Cor | Onde | Texto |
|---|---|---|---|
| `t-cream` | `#FFFBF0` | leitura longa | navy sobre creme |
| `t-white` | `#F9FAFB` | idem, alternando com o creme | navy sobre branco |
| `t-navy` | `#002966` | heros e secções de destaque | creme |
| `t-blue` | `#0047B2` | uma faixa por página, no máximo | creme |
| `t-ink` | `#001433` | header, rodapé, CTA final | creme |

Nenhuma página tem duas superfícies iguais seguidas nem repete a sequência de outra.

**Dentro de um painel de cor, os cartões são transparentes** com borda e texto em creme.
Cartões creme dentro de um painel azul, numa página clara, faziam o painel ler-se como
uma moldura em vez de um bloco de cor — e o azul quase desaparecia.

Duas regras verificadas automaticamente: nunca um botão laranja dentro de um painel azul
(o laranja só separa 2.88:1 do azul), e nunca duas superfícies claras iguais seguidas.

---

## 6. Fotografia

Quatro fotos do espaço em `assets/fotos/`, em duas larguras, servidas por `srcset` com
`sizes`, `width`/`height` declarados e `loading="lazy"` fora do primeiro ecrã.

| Ficheiro | Onde |
|---|---|
| `hero-recepcao` (21:8) | hero da homepage |
| `hero-fachada` (21:8) | hero de contactos — ajuda a encontrar a porta |
| `sala-1` (3:2) | hero de `pais`, galeria de `sobre`, `como-funciona` |
| `sala-2` (3:2) | hero de `alunos`, galeria de `sobre` |
| `recepcao` (3:2) | galeria de `sobre`, `como-funciona` |
| `fachada` (3:2) | galeria de `sobre` |

Todas com `alt` descritivo do que se vê, não do ficheiro.

**Falta a fotografia da equipa**, e é o que mais falta no site. As caras são o que fecha
uma recomendação.

---

## 7. Acessibilidade

Auditado contra WCAG 2.1 AA a cada alteração. Zero problemas.

| Critério | Como está resolvido |
|---|---|
| 1.1.1 Conteúdo não textual | SVG decorativos com `aria-hidden` e `focusable="false"`; logótipo com `alt`; fotos com `alt` descritivo; botão de WhatsApp com `aria-label` |
| 1.3.1 Informação e relações | `<main>`, `<nav aria-label>`, `<header>`, `<footer>`; títulos sem saltos de nível |
| 1.4.3 Contraste do texto | Mínimo medido 5.39:1. Todos os pares em uso acima de 4.5 |
| 1.4.4 Redimensionar texto | Tudo em `rem`; sem `user-scalable=no` |
| 1.4.11 Contraste não textual | Bordas, contornos de botão e hairlines acima de 3:1 nos cinco tons |
| 2.1.1 Teclado | Só HTML nativo: links, botões e `<details>` |
| 2.4.1 Ignorar blocos | Link "Saltar para o conteúdo" em todas as páginas |
| 2.4.2 Título da página | `<title>` único e descritivo |
| 2.4.4 Contexto do link | Nenhum "clique aqui" |
| 2.4.7 Foco visível | Anel de 3px com contraste adaptado a cada tom |
| 2.5.8 Tamanho do alvo | Botões com 44px de altura mínima |
| 3.1.1 Idioma | `lang="pt-PT"` |
| 2.3.3 Movimento | `prefers-reduced-motion` respeitado |

**Uma correção em relação às peças de comunicação.** A peça da citação de Aristóteles usa
creme sobre laranja: 2.77:1, abaixo de qualquer mínimo. Num cartão de Instagram passa;
num site com parágrafos, não.

---

## 8. Rótulos e CTAs

Um destino, um rótulo:

| Destino | Rótulo |
|---|---|
| `inscricao.html` | Fazer a inscrição |
| `tel:` | Ligar 214 100 902 |
| `wa.me` | WhatsApp 964 989 883 |
| `mailto:` | Enviar email |
| `disciplinas.html` | Ver todas as disciplinas |

Duas exceções deliberadas: na barra fixa de mobile o telefone diz só "Ligar", porque o
número não cabe; e na inscrição há dois botões de WhatsApp, "com a lista de campos" e
"em branco", porque são ações diferentes.

**Botão 1:1 do WhatsApp** fixo no canto inferior direito das oito páginas.

---

## 9. O que falta preencher

32 marcadores.

### Bloqueiam o lançamento

| Onde | O que falta | Valor |
|---|---|---|
| `inscricao.html` | Ficheiro PDF da ficha de inscrição | |
| `inscricao.html` | Lista definitiva de campos da ficha | |
| `pais` · `como-funciona` | Duração padrão de uma explicação | |
| FAQ | Métodos e momento de pagamento | |

### Regras e políticas

| Onde | O que falta | Valor |
|---|---|---|
| `pais.html` | Existe relatório de progresso? Com que frequência e formato? | |
| `pais` · `alunos` | Condições para trocar de explicador | |
| FAQ | As horas compradas expiram? | |
| FAQ | Antecedência para desmarcar sem perder a hora | |
| FAQ | Aceitam alunos fora de setembro? | |
| `alunos.html` | Há formato intensivo pré-exame? | |

### Conteúdo de páginas

| Onde | O que falta | Valor |
|---|---|---|
| `alunos.html` | Cadeiras do superior cobertas com segurança | |
| `disciplinas.html` | Lista real, por nível | |
| `sobre.html` | Nomes, formação e uma linha por explicador | |
| `sobre.html` | Desde quando existe o centro | |
| `sobre.html` | Quantos alunos acompanha por ano | |
| `como-funciona.html` | Como é atribuído o explicador | |

### Recolhas

- [ ] Fotografia da equipa (o espaço já está fotografado)
- [ ] 6 a 10 testemunhos com nome, ano e disciplina, com autorização escrita

---

## 10. Falta ligar

- **Mapa.** Os blocos `.map` são placeholders. Incorporar Google Maps ou OpenStreetMap.
- **Schema markup** `LocalBusiness` com morada, horário e telefones.
- **Google Business Profile** com as mesmas fotos, horário e morada. Sem campanhas, é o
  canal que traz mais gente.

---

## 11. Uma contradição por resolver

O Manual de Normas Gráficas descreve centro de estudos como quem "ministra explicações
individuais **e em grupos**". O site assume só individual, como confirmado. Se houver
grupos, mudam várias secções.
