# Melhores práticas para o Git

Repositório criado para auxiliar a mim e a você no uso das melhores práticas go Git.

Viu a oportunidade de melhorar de alguma forma o repositório? Sinta-se à vontade para contribuir 🙂

## Branches (Padrão Gitflow)

### Ideia

O GitFlow é um modelo de fluxo de trabalho do Git que oferece uma estrutura robusta para gerenciamento de projetos.

Ele define um conjunto de regras para criar e integrar diferentes branches no desenvolvimento, permitindo que várias funcionalidades sejam desenvolvidas em paralelo, preparação para novos lançamentos e correções de bugs rápidas e eficientes.

É especialmente útil em projetos grandes com várias pessoas trabalhando simultaneamente.

### Imagem de exemplo

<br />
<img height="400em" src="./images/01_branches.svg" align="center" />
<br />

### Padrão de branches

- `main` é a branch principal do projeto. É considerada a versão de produção estável do código. **Não se escreve código, somente recebe do develops, release e hotfix**
- `develops` é a branch de desenvolvimento contínuo, onde as features são integradas. **Não se escreve código, somente recebe de outras branches**
- `feature` são as branches criadas para desenvolver novas funcionalidades.
- `release` são as branches criadas para preparar o código para um release (correção de bugs, ajustes finos e preparação para a versão de produção). Separamos aqui o que está pronto para produção  do que ainda não está.
- `hotfix` são as branches criadas para corrigir bugs na produção.

### Orientações

- Criar branches com os prefxos acima + a ideia da branche
  - Exemplo: feature/mostrar_vizualizacao
- Criar branches de release com a nova versão do aplicativo
  - Exemplo: release/0.1.0
  - O primeiro número aumenta quando a nova versão não é compativél com a primeira.
  - O segundo número aumenta quando uma nova funcionalidade é adicionada.
  - O terceiro número aumenta quando foi corrigido um erro que foi para produção.

## Commits Semânticos

- `feat` é para adições de novas funcionalidades ou de quaisquer outras novas implantações ao código;
- `fix` refere-se às correções de bugs;
- `docs` referem-se a inclusão ou alteração somente de arquivos de documentação;
- `perf` é para alteração de código que melhora o desempenho;
- `refactor` é utilizado em quaisquer mudanças que sejam executados no código, porém não alterem a funcionalidade final da tarefa impactada;
- `style` é usadado para alterações referentes a formatações na apresentação do código que não afetam o significado do código, como por exemplo: espaço em branco, formatação, ponto e vírgula ausente etc.);
- `test` é para adicionar testes ausentes ou corrigindo testes existentes nos processos de testes automatizados (TDD);
- `env` é basicamente utilizado na descrição de modificações ou adições em arquivos de configuração em processos e métodos de integração contínua (CI).





