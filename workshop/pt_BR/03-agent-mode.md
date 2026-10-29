<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o jogo com fluxos de trabalho agênticos

---

Nesta parte, o Copilot passa de planejador a implementador. Em vez de escrever código linha por linha, descreva o que deseja e deixe o Copilot trabalhar nos arquivos necessários.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Insira este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Volte o Copilot CLI ao fluxo normal de programação (ou continue no modo autopilot se quiser que ele prossiga até você pará-lo).
2. Se for útil, mencione o arquivo da página para fornecer mais contexto: `@src/pages/index.astro`.
3. Insira este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript do lado do cliente à página de batalha para que:
   > 1. Ao clicar no botão Battle, os dois nomes de usuário sejam obtidos dos campos.
   > 2. Verifique se ambos foram preenchidos (e mostre um erro caso contrário).
   > 3. Busque em paralelo na nossa API os dados de contribuição dos dois usuários.
   > 4. Renderize os gráficos de contribuições em grades coloridas, com um quadrado por dia, usando a paleta de cores do GitHub.
   > 5. Mostre um selo VS entre os dois usuários.
   > 6. Exiba o nome de usuário, o total de contribuições e o intervalo de datas de cada usuário.
   > 7. Trate os estados de carregamento e os erros.
   > 8. Dispare a batalha também ao pressionar Enter nos campos.
   > 9. Use a interface simples que já está preparada.
   >
   > Use interfaces do TypeScript para a estrutura dos dados de contribuição.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI implementar as alterações em `src/pages/index.astro`.
5. Use `/diff` para inspecionar as alterações geradas e depois aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não for atualizada, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador.

1. Insira `octocat` e `torvalds` como nomes de usuário e clique em **Battle**.
2. Você deve ver os dois gráficos de contribuição lado a lado, com grades coloridas.
3. Teste os casos de erro:
   - Deixe um ou ambos os campos vazios e clique em Battle: deve aparecer um erro de validação.
   - Insira um nome de usuário inválido: o aplicativo deve exibir um erro da API.
4. Pressione **Enter** em qualquer campo; isso deve iniciar a batalha como se você tivesse clicado no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver bem como esperado, envie feedback diretamente ao Copilot. Por exemplo:

- *Os quadrados de contribuição estão grandes demais; ajuste-os para 12x12 px.*
- *Adicione uma dica ao passar o cursor que mostre a data e a contagem de contribuições.*
- *O estado de carregamento precisa de uma animação de pulso.*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e iterações. Cada prompt de acompanhamento se baseia na conversa anterior, permitindo refinar a implementação aos poucos sem recomeçar.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento se baseia no anterior. Use `/session` ou `/context` para inspecionar o contexto que o Copilot está mantendo e `/review` depois de uma iteração maior para procurar bugs ou melhorias.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que deseja**: requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las**: inspecionar o diff é mais rápido do que reescrever o código depois.
- **Teste o aplicativo após cada implementação** para localizar problemas.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**.
- **Iterar nos resultados** com feedback direcionado.
- Seguir o **ciclo completo de uma funcionalidade**: implementação, revisão, testes e refinamento.
