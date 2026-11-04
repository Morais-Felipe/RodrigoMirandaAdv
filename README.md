# Rodrigo Miranda | Advocacia de trânsito

Landing page de Rodrigo Miranda, que atua com recursos de multas e processos de trânsito em Uberaba (MG) e em todo o Brasil.

O objetivo é simples: quem recebeu uma notificação encontra as informações principais e chega ao WhatsApp em poucos toques. O site também serve de destino para o QR Code do panfleto.

## O que tem na página

- **Início:** apresentação e botão de WhatsApp com mensagem pronta
- **Áreas de atuação:** recusa ao bafômetro, excesso de velocidade, exame toxicológico, multas em geral, suspensão e cassação da CNH
- **Como funciona:** do primeiro contato à defesa, em quatro passos
- **Sobre e dúvidas frequentes**
- **Contato:** endereço, horários e e-mail

## Tecnologias

- [Astro](https://astro.build): gera a página como HTML estático
- CSS e JavaScript puros para o visual e as animações
- Playfair Display e Inter, servidas pelo próprio site via Fontsource
- [Vercel](https://vercel.com) para a hospedagem

Não há banco de dados, login nem formulário: o conteúdo fica no código.

## Como rodar

É preciso ter o [Node.js](https://nodejs.org) instalado.

```bash
npm install
npm run dev
```

O site abre em http://localhost:4321.

| Comando | O que faz |
|---|---|
| `npm run dev` | Inicia o ambiente de desenvolvimento |
| `npm run build` | Gera o site final na pasta `dist/` |
| `npm run preview` | Mostra localmente o site gerado |

## Como editar

Quase tudo está em [`src/pages/index.astro`](src/pages/index.astro):

- **Textos das áreas, passos e dúvidas:** listas `areas`, `passos` e `faq`, no início do arquivo
- **WhatsApp, e-mail e endereço:** constantes `wa`, `email` e `endereco`, também no início (o número exibido na seção de contato fica no HTML)
- **Cores:** variáveis em `:root`, no bloco de estilos
- **Foto:** `public/rodrigo-miranda.webp`

As animações respeitam a opção "reduzir movimento" do aparelho.

## Publicação na Vercel

1. Importe este repositório na Vercel.
2. Mantenha o framework detectado (Astro), com o comando `npm run build` e a pasta `dist`.
3. Depois disso, cada push na branch de produção publica uma nova versão.

## Antes de publicar

- [ ] Revisão dos textos por Rodrigo, considerando as regras de publicidade da OAB
- [ ] Decisão sobre exibir o número de inscrição na OAB
- [ ] Domínio próprio configurado

## Autor

Desenvolvido por [Felipe Morais](https://github.com/Morais-Felipe).
