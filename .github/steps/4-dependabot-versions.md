## Passo 4: Habilitar e acionar atualizações de versão do Dependabot

_Muito bem!_ :partying_face:

Agora você automatizou o processo para o Dependabot alertá-lo sobre vulnerabilidades em suas dependências e criar pull requests para atualizá-las para versões seguras! Neste ponto, você só precisa revisar o pull request e, em seguida, fazer o merge para ficar em dia com os problemas de segurança das dependências.

O recurso de atualizações de segurança ajuda a automatizar o processo de resolver alertas, mas e quanto a apenas manter-se atualizado com as atualizações de versão? Também podemos automatizar a geração de pull requests para versões atualizadas das dependências usando o recurso de atualizações de versão do Dependabot.

**O que são atualizações de versão do Dependabot?**: Além dos alertas de segurança, o Dependabot também pode tirar o esforço de manter suas dependências. Você pode usá-lo para garantir que seu repositório acompanhe automaticamente os últimos lançamentos dos pacotes e aplicações dos quais depende. Semelhante aos alertas de segurança, o Dependabot identificará uma dependência desatualizada e criará um pull request para atualizar o manifesto para a versão mais recente da dependência.

Vamos ver como isso funciona!

### :keyboard: Atividade 4.1: Habilitar e acionar atualizações de versão do Dependabot

1. Navegue até a aba **Settings** e selecione **Advanced Security**.
2. Localize "Dependabot version updates" e clique em **Configure** para abrir um novo editor de arquivos com conteúdo pré-preenchido. O arquivo é chamado `dependabot.yml`.
3. Observe que o arquivo está pré-preenchido para atualizar as ações do GitHub no repositório, o ecossistema de pacotes `github-actions`.
4. Copie as linhas que definem as atualizações das ações do GitHub e as adicione ao arquivo.
5. Edite sua cópia do conteúdo:
   - Altere o `package-ecosystem` para `nuget`.
   - Altere o `directory` para `/code/`.
   - Altere o `interval` para `weekly`.
   
   O arquivo `dependabot.yml` deve agora ficar assim.
   ```yaml
   version: 2
   updates:
     - package-ecosystem: "github-actions"
       directory: "/"
       schedule:
         interval: "monthly"
     - package-ecosystem: "nuget"
       directory: "/code/"
       schedule:
         interval: "weekly"
    ```
6. Faça o commit das suas alterações diretamente na branch `main`.

Você agora configurou as atualizações de versão do Dependabot para executar e verificar atualizações da seguinte forma:
- Verificar uma vez por mês por atualizações das ações do GitHub e criar pull requests para atualizar quaisquer que estejam desatualizadas.
- Verificar uma vez por semana por atualizações de pacotes .NET e criar pull requests para atualizar quaisquer que estejam desatualizadas. Por padrão, essa verificação é executada na segunda-feira. Para executar a verificação em um dia diferente, veja [schedule.day](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file#scheduleday).

Espere cerca de 20 segundos e então atualize esta página (a página onde você está seguindo as instruções). [GitHub Actions](https://docs.github.com/en/actions) será atualizado automaticamente para exibir o próximo passo.
