# Agenda Alimentar — Mauricio

Site pessoal de organização do plano alimentar (café da manhã, almoço, lanches,
jantar, ceia), água, suplementação e relatório mensal de acompanhamento.

Não é uma prescrição nova: organiza o plano já elaborado pela nutricionista.
Não calcula calorias nem macronutrientes.

## Como publicar no GitHub Pages

1. Crie um repositório novo (pode ser público) e envie o arquivo `index.html`
   para a raiz do repositório.
2. Vá em **Settings → Pages**.
3. Em "Branch", selecione `main` e a pasta `/root` (raiz), depois **Save**.
4. Em alguns minutos o link do site aparece na mesma tela ("Your site is live at...").
5. No celular, abra esse link e use "Adicionar à tela inicial" (Android) ou
   "Adicionar à Tela de Início" (iPhone) para que ele funcione como um app.

## Importante sobre os dados

Os dados (refeições marcadas, água, observações, avaliações, relatório
mensal) ficam salvos **no navegador de cada aparelho** (localStorage) — não
em um servidor. Isso significa:

- Os dados não se sincronizam automaticamente entre o celular e o computador.
- Trocar de navegador (ex.: sair do Chrome para o Safari) ou limpar os dados
  de navegação apaga o histórico.
- Use sempre o mesmo navegador, no mesmo aparelho, para manter o histórico
  contínuo do relatório mensal.

## Estrutura de dados (para editar quantidades depois)

Dentro do `<script>` do `index.html`:

- `cafeDaManha`, `lanchesTarde`, `jantares`: bancos de opções de refeição.
- `proteinasPool`, `carboidratosPool`, `legumesPool`: opções do almoço.
- `cardapioOriginal`: cardápio padrão de cada dia da semana.
- `estado.dias`: trocas de cardápio feitas (por dia da semana, se repetem
  toda semana).
- `estado.registros`: histórico real por data (o que alimenta o relatório
  mensal).
