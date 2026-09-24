# Contrato Digital — MPS Photography

Site único (HTML/CSS/JS, sem backend) para gerar, enviar e assinar contratos digitalmente.

## Como publicar no GitHub Pages
1. Crie um repositório no GitHub (ex: `Contrato-MPS-Photography`).
2. Suba o arquivo `index.html` para a raiz do repositório.
3. Vá em Settings → Pages → Branch: main / (root) → Save.
4. Aguarde alguns minutos; o link ficará algo como:
   `https://SEU-USUARIO.github.io/Contrato-MPS-Photography/`

## Como usar
1. Abra o link do site (sem nenhum parâmetro na URL) — isso mostra o **painel da fotógrafa**.
2. Preencha os dados do serviço já combinados com a cliente (tipo de ensaio, pacote, data, valores, forma de pagamento etc.) e clique em **"Gerar link do contrato"**.
3. Copie o link gerado e envie para a cliente pelo WhatsApp.
4. A cliente abre o link, preenche os dados pessoais dela (nome, CPF, telefone, e-mail, endereço) e escolhe as opções de **direitos de imagem** — tudo na mesma página.
5. Em seguida, o contrato completo aparece para ela ler e assinar digitalmente (assinatura por toque/mouse).
6. Depois de assinar, ela pode salvar o contrato em PDF (via impressão do navegador) e enviar de volta pelo WhatsApp.

## Observação sobre valores
Se a cliente pedir fotos extras além do pacote combinado, o valor final deve ser combinado diretamente com a fotógrafa **antes** de gerar/enviar o link do contrato, já que o valor é definido pela fotógrafa no painel.

## Onde editar os preços dos pacotes
Ao escolher o "Tipo de serviço" no painel (Gestante, Newborn, Casal, etc.), aparecem sugestões de pacotes (Essencial/Especial/Completo) com valores — ao tocar em um, o valor e a descrição são preenchidos automaticamente (mas dá pra editar na mão depois também).

**Esses valores são só um ponto de partida (placeholder) — ajuste para a sua realidade.** Para editar:

1. Abra o arquivo `index.html` em qualquer editor de texto (Bloco de Notas, VS Code, etc.).
2. Use Ctrl+F e procure por `const PACOTES`.
3. Você vai ver um bloco assim, um grupo para cada tipo de ensaio:
   ```js
   'Ensaio Gestante': [
     { nome: 'Essencial', valor: 300, desc: '10 fotos editadas em alta resolução' },
     { nome: 'Especial',  valor: 500, desc: '20 fotos editadas + 1 foto impressa 20x30' },
     { nome: 'Completo',  valor: 750, desc: '35 fotos editadas + álbum físico' },
   ],
   ```
4. Troque o número depois de `valor:` e o texto depois de `desc:` (mantenha as aspas). Não precisa mexer em mais nada.
5. Salve o arquivo e suba de novo pro GitHub (substituindo o `index.html` do repositório) — a página atualiza sozinha.

A mesma tabela de preços é usada para gerar a placa de valores em A4 (peça pra eu gerar de novo se você mudar os valores).
