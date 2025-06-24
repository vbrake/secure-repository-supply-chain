## Passo 1: Revisar e adicionar dependências usando o gráfico de dependências

_Bem-vindo ao "Proteja a cadeia de suprimentos do seu repositório"! :wave:_

**Qual é a importância de proteger a cadeia de suprimentos do seu repositório?**: Com o uso acelerado de código aberto, a maioria dos projetos depende de centenas de dependências de código aberto. Isso representa uma questão de segurança [...]

O GitHub oferece uma série de recursos para ajudá-lo a entender as dependências em seu ambiente, conhecer as vulnerabilidades dessas dependências e corrigi-las. Os recursos da cadeia de suprimentos no GitHub incluem:

- Gráfico de dependências
- Revisão de dependências
- Alertas do Dependabot
- Atualizações do Dependabot
  - Atualizações de segurança do Dependabot
  - Atualizações de versão do Dependabot

**O que é um gráfico de dependências**: O gráfico de dependências é um resumo dos arquivos de manifesto e de bloqueio armazenados em um repositório e quaisquer dependências que são submetidas ao repositório usando o Depend[...]

- Dependências, os ecossistemas e pacotes dos quais depende
- Dependentes, os repositórios e pacotes que dependem dele

### :keyboard: Atividade 1.1: Verificar se o gráfico de dependências está habilitado

**Recomendamos abrir outra aba do navegador para realizar as atividades a seguir, assim você pode manter estas instruções abertas para referência.**

O gráfico de dependências está habilitado por padrão para todos os novos repositórios públicos. Se você estiver trabalhando em um repositório público, pode ir direto para "Atividade 1.2: Adicionar uma nova dependência e visualizar seu gráfico de dependências".

1. Navegue até a aba **Settings**.
2. Clique em **Advanced Security**.
3. Habilite **Dependency graph**.

### :keyboard: Atividade 1.2: Adicionar uma nova dependência e visualizar seu gráfico de dependências

1. Navegue até a aba **Code** e localize a pasta `code/src/AttendeeSite`.
2. Adicione o seguinte conteúdo ao arquivo `package-lock.json` após a terceira chave `}` antes das duas últimas chaves.
    ```
    ,
     "follow-redirects": {
       "version": "1.14.1",
       "resolved": "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",
       "integrity": "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="
     }
    ```
3. Navegue até a aba **Insights**.
4. Selecione **Dependency graph** na barra de navegação lateral.
5. Revise todas as dependências na aba **Dependencies**.
6. Pesquise por `follow-redirects` e revise a nova dependência que você acabou de adicionar.
    ![Captura de tela mostrando a dependência "follow-redirects".](https://user-images.githubusercontent.com/6351798/196288729-734e3319-c5d7-4f35-a19c-676c12f0e27d.png)

Espere cerca de 20 segundos e então atualize esta página (a página onde você está seguindo as instruções). [GitHub Actions](https://docs.github.com/en/actions) será atualizado automaticamente para exibir o próximo passo.
