# Contrato Digital — MPS Photography

Site estático (HTML puro) para gerar, enviar e assinar digitalmente o contrato de
prestação de serviços de fotografia/filmagem. Não depende de nada exclusivo do Claude —
roda normal no GitHub Pages, igual a Galeria de Entrega.

## Como publicar (mesmo fluxo dos outros dois projetos)

1. Cria um repositório novo no GitHub (ex: `Contrato-MPS-Photography`).
2. Sobe o `index.html` desta pasta (upload direto, sem subpastas).
3. Em Settings → Pages, ativa o GitHub Pages na branch main.
4. O link final fica tipo: `https://prhyiscyillah.github.io/Contrato-MPS-Photography/`

## Como usar

- Link sem parâmetro → abre o painel pra você criar um contrato novo (dados do cliente,
  tipo de serviço, pacote, valores, direitos de imagem etc).
- Ao gerar, ele monta um link `?d=XXXX` — esse é o que você envia pro cliente assinar.
- O cliente vê o contrato completo, assina no campo de assinatura, e usa o botão
  "Salvar PDF / Imprimir" (funciona em qualquer celular, com ou sem conta Claude).

## Observação

O botão secundário "Tentar baixar PDF automaticamente" só funciona de verdade dentro do
Claude (usa um recurso exclusivo daqui). Fora do Claude, ele tenta abrir o PDF numa aba
nova como alternativa — o botão principal "Salvar PDF / Imprimir" é o que sempre funciona,
em qualquer navegador.
