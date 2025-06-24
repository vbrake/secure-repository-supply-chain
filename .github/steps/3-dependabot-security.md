## Passo 3: Habilitar e acionar atualizações de segurança do Dependabot

_Bom trabalho habilitando, visualizando e criando alertas do Dependabot :sparkles:_

Habilitar alertas do Dependabot no nosso repositório foi um ótimo passo para melhorar a segurança do nosso código, mas ainda tivemos que selecionar manualmente um alerta e depois selecionar manualmente a opção de criar o pull request. Seria bom melhorar ainda mais a automação e manutenção de nossas dependências! Bem, com as atualizações de segurança do Dependabot, podemos fazer exatamente isso.

**O que são atualizações de segurança do Dependabot?**: Quando este recurso está habilitado, o Dependabot detecta *e* corrige dependências vulneráveis para você, abrindo pull requests automaticamente para resolver alertas do Dependabot.

Criamos manualmente um pull request para corrigir o alerta "Prototype Pollution in minimist", mas vamos habilitar atualizações de segurança do Dependabot para automatizar esse processo para futuros alertas!

### :keyboard: Atividade 3.1: Habilitar e acionar atualizações de segurança do Dependabot

1. Navegue até a aba **Settings** e selecione **Advanced Security**.
2. Habilite **Dependabot security updates**. Pode ser necessário esperar de 30 a 60 segundos antes de ver novos pull requests.
3. Navegue até a aba **Pull requests** do repositório e selecione o pull request recém-criado.
4. Revise e faça o merge do pull request.

Espere cerca de 20 segundos e então atualize esta página (a página onde você está seguindo as instruções). [GitHub Actions](https://docs.github.com/en/actions) será atualizado automaticamente para exibir o próximo passo.
