<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Temas orientados ao design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para criar uma transformação completa do tema. Esta é uma abordagem de desenvolvimento orientada ao design: comece com a visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de arcade retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon no título pulsando como um letreiro, selo VS animado com mudanças nas cores do gradiente, sobreposição de brilho nas placas de resultados dos usuários, animações de entrada flutuante nos campos, texto de carregamento alternando entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuição. Mantenha o fundo escuro (`#0a0a1a`) com as cores de destaque verde (`#5fed83`) e roxo (`#8a2be2`). Use um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado que cobre todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes na duração das animações (por exemplo, *"Deixe o pulso neon mais lento, com cerca de 3 segundos"*).
- Pergunte sobre efeitos específicos (por exemplo, *"Como vai funcionar a sobreposição de brilho nas placas?"*).
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de arcade retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudo-elementos e transições à sua folha de estilos. Isso pode incluir:

- `@keyframes` para linhas de varredura, pulso neon, brilho e efeitos de entrada flutuante.
- Pseudo-elementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades customizadas de CSS para as cores do tema.
- Transições e estados ao passar o cursor sobre elementos interativos.

<!-- track:cli:start -->
Quando as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor (`Ctrl+C`), reinicie com `npm run dev` e atualize a página forçando o recarregamento (`Ctrl+Shift+R`).

Mantenha a prévia do navegador aberta e itere no design. Experimente prompts como:

> O efeito das linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma oscilação elétrica sutil ao texto do título.

> O selo VS deveria pulsar com mais intensidade.

Esta é uma **abordagem de desenvolvimento orientada ao design**: você está iterando no resultado visual em tempo real. Cada prompt refina a experiência até ficar como você deseja. Não se contente com algo "bom o suficiente" — aperfeiçoe o visual até a página parecer pertencer a um fliperama.

## Tarefa 4: Atualize as instruções

As instruções devem refletir as principais decisões de design para manter os prompts futuros alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione uma seção de guia de design a `copilot-instructions.md` descrevendo o tema de arcade retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um breve guia de design para o tema de arcade retrô: cores, fontes, estilo das animações e a regra de que novas interfaces devem manter a estética neon.
<!-- track:cli:end -->

Quando a página estiver como você deseja, faça commit das instruções e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para esboçar um **sistema de design antes da implementação**.
- **Iterar no resultado visual** com prompts de acompanhamento.
- **Atualizar as instruções após decisões importantes** para manter a identidade visual consistente.
