# Dumnus Hub — Landing Page

Página única de conversão. **Um só objetivo: agendamento pelo WhatsApp.**
Sem menu, sem links que tiram o visitante da página. Todos os 6 botões levam
para o mesmo lugar: `wa.me/5519991030274`.

- Arquivo da página: `index.html` (tudo embutido — CSS e imagens, sem build)
- Imagens: `assets/`
- É só abrir o `index.html` no navegador ou subir a pasta em qualquer hospedagem.

---

## Estado atual

**Modo rascunho desligado.** Não há mais nenhum campo pendente na página.

Preenchido: endereço, horários, os quatro serviços, sobrancelha de
cortesia, formas de pagamento (dinheiro, Pix e cartão), atendimento a crianças
de todas as idades, e o bloco "Quem corta" com a foto do Vitor Tavares,
barbeiro há mais de 3 anos.

Mídia em `assets/`:

| Pasta | Conteúdo |
|---|---|
| `fotos/` | 8 fotos de cortes para a galeria (800×1000) |
| `videos/` | 14 clipes de cortes com capa (carrossel) |
| `espaco/` | foto do salão e 2 vídeos do espaço, com capas |
| `vitor.jpg` | retrato do barbeiro |

Os vídeos só baixam quando alguém toca no play. Para trocar um arquivo,
mantenha o nome e a proporção.

### Preços (guardados, fora da página por enquanto)

A tabela mostra os serviços sem valor, com "Consulte no WhatsApp". Quando
quiser publicar os preços, eles eram: corte a partir de R$ 29,99 · barba
R$ 19,99 · alisamento R$ 24,99 · acabamento (pezinho) R$ 14,99.

### Vale acrescentar depois

**Depoimentos.** É a única prova social que ainda falta. A seção já existe,
escondida, no fim da galeria: quando tiver 2 ou 3 avaliações reais (print do
WhatsApp ou Google), é só me mandar.

**Tempo médio de atendimento.** A pergunta "Quanto tempo demora?" foi retirada
da FAQ porque não havia resposta. Com o tempo médio do corte e da barba, ela
volta.

---

## Garantia e SEO local

**Garantia de ajuste gratuito.** Procure por `SECAO 10` no `index.html`. Está
pronta, comentada. É a resposta mais forte para o "e se eu não gostar do corte"
— só ative se for honrar o prazo.

**SEO local (JSON-LD).** Ativo no fim do arquivo, com nome, endereço, CEP,
telefone, horários, faixa de preço, formas de pagamento e o barbeiro.

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

Abra o endereço `.vercel.app` no celular, toque num botão e confira que abre o
WhatsApp certo. Dê play num clipe. Pronto para anunciar.
