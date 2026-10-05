# Dumnus Hub — Landing Page

Página única de conversão. **Um só objetivo: agendamento pelo WhatsApp.**
Sem menu, sem links que tiram o visitante da página. Todos os 6 botões levam
para o mesmo lugar: `wa.me/5519991030274`.

- Arquivo da página: `index.html` (tudo embutido — CSS e imagens, sem build)
- Imagens: `assets/`
- É só abrir o `index.html` no navegador ou subir a pasta em qualquer hospedagem.

---

## Falta você preencher

A página está em **modo rascunho**: tudo que precisa do seu dado real aparece
**destacado em amarelo** na tela. Não inventei nenhuma informação.

### ~~1. As 4 fotos dos cortes~~ ✅ feito

As quatro fotos já estão em `assets/fotos/`, em 800×1000 (proporção 4:5),
cerca de 120 KB cada, e só carregam quando o visitante rola até a galeria.
Para trocar alguma, exporte no mesmo formato e mantenha o nome do arquivo.

### 2. Os preços

Procure por `R$` na seção de serviços e troque os `--` pelos valores dos três
serviços: Corte + Barba, Corte/Degradê e Barba na navalha.

### 3. Horários e dados do atendimento

O **endereço já está preenchido**: Rua Regina Consulin Escalhão, 1021 —
Jd. Maria Antônia, Sumaré/SP (CEP 13178-380). Aparece no topo, no rodapé,
na FAQ e nos dados de SEO local, com link para o mapa.

Ainda faltam, todos destacados em amarelo:

- dias e horários de funcionamento
- formas de pagamento
- tempo médio de atendimento (FAQ)
- se atende criança e a partir de que idade (FAQ)
- se tem sábado ou horário estendido (quebra de objeções)
- se tem estacionamento por perto (FAQ)

Ao preencher os horários, abra também a linha `openingHours` no bloco de
SEO local, no fim do `index.html`, no formato 24h (ex: `"Tu-Sa 09:00-19:00"`).

### 4. O bloco "Por que confiar sua cabeça aqui"

Seu nome, há quantos anos corta, com quem aprendeu e o jeito de trabalhar.
**Deixei em branco de propósito** — autoridade inventada é a forma mais rápida
de perder a confiança de um cliente local, que cedo ou tarde te encontra pessoalmente.

---

## Quando terminar de preencher

Na **linha 2** do `index.html`, troque:

```html
<html lang="pt-BR" data-draft="on">
```

por:

```html
<html lang="pt-BR">
```

Isso apaga a tarja de aviso do topo e todos os destaques amarelos de uma vez.
**Faça isso antes de divulgar o link.**

---

## Duas coisas que valem ativar depois

Estão prontas no código, comentadas, esperando sua decisão:

**Garantia de ajuste gratuito.** Procure por `SECAO 10` no arquivo. É a resposta
mais forte para o "e se eu não gostar do corte" — mas só ative se você for mesmo
honrar o prazo. Defina em quantos dias e para quais serviços.

**SEO local (JSON-LD).** Já está **ativo** no fim do arquivo, com nome, endereço,
CEP, telefone e link do mapa — é o que ajuda a barbearia a aparecer na busca por
"barbearia em Sumaré". Falta só acrescentar os horários quando você confirmar.

---

## O que ainda falta para a página ficar completa

**Depoimentos.** Com as fotos no ar, é o que falta de prova social.
A seção já existe e está vazia de propósito — não escrevi nenhum depoimento fictício.
Assim que você tiver avaliações reais (Google, Instagram ou print do WhatsApp),
é só mandar que eu encaixo.

---

## Arquivos de imagem

| Arquivo | Uso |
|---|---|
| `assets/logo.png` | logo usada na página (fundo transparente, 28 KB) |
| `assets/logo-512.jpg` | ícone da aba e imagem de compartilhamento no WhatsApp/redes |
| `assets/logo.jpg` | original enviado, guardado como referência (não é usado na página) |

---

## Subir na Vercel

O site é estático, sem build. A Vercel serve a pasta direto.

### 1. Importe o repositório

Entre em **https://vercel.com/new**, conecte sua conta do GitHub e escolha o
repositório `manovares/dummnus`.

Na tela de configuração, deixe tudo como vem:

| Campo | Valor |
|---|---|
| Framework Preset | **Other** |
| Build Command | *(vazio)* |
| Output Directory | *(vazio — a raiz)* |
| Install Command | *(vazio)* |

Clique em **Deploy**. Em menos de um minuto o site está no ar.

### 2. Aponte para a branch certa

O código está na branch `claude/peaceful-fermi-imcsp5`, e a Vercel publica a
branch de produção (por padrão `main`, que este repositório ainda não tem).

Em **Settings → Git → Production Branch**, troque para
`claude/peaceful-fermi-imcsp5` e salve. A partir daí, todo push nessa branch
republica o site sozinho.

### 3. Domínio

A Vercel dá um endereço `.vercel.app` de graça, que já serve para anunciar.
Para usar um domínio próprio (ex: `dumnushub.com.br`), compre o domínio e
aponte em **Settings → Domains**; a Vercel mostra os registros de DNS a criar
e emite o certificado HTTPS sozinha.

### Antes de divulgar o link

Desligue o modo rascunho (`data-draft="on"`, explicado acima) e confira que
nenhum trecho amarelo ficou na página. Enquanto houver `R$ --` e textos
começando com `PREENCHA`, qualquer visitante os enxerga.
