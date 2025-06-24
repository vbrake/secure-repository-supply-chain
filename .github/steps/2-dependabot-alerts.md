## Passo 2: Habilitar e visualizar alertas do Dependabot

_Bom trabalho! :tada: Você adicionou e visualizou uma dependência usando o gráfico de dependências!_

Dado o número de dependências que nosso repositório utiliza, manter essas dependências precisa se tornar uma tarefa automatizada. Manter nosso código seguro é uma prioridade, então a primeira coisa que precisamos fazer é configurar uma forma de sermos notificados quando uma dependência que estamos usando é vulnerável ou contém malware. Podemos fazer isso habilitando alertas do Dependabot.

**O que são alertas do Dependabot?**: Alertas do Dependabot informam que seu código depende de um pacote inseguro. Esses alertas do Dependabot referenciam a [Base de Dados de Consultoria do GitHub](https://github.com/advisories), que contém uma lista de vulnerabilidades de segurança e malware conhecidos, agrupados em duas categorias: **Consultorias revisadas pelo GitHub** e **Consultorias não revisadas**.

Se seu código depende de um pacote que tem uma vulnerabilidade de segurança, isso pode causar uma série de problemas para o seu projeto ou para as pessoas que o utilizam. Você deve atualizar para uma versão segura do pacote o mais rápido possível. Se seu código utiliza malware, você precisa substituir o pacote por uma alternativa segura.

Vamos testar isso com nossa recém-adicionada dependência `follow-redirects`!

### :keyboard: Atividade 2.1: Visualizar consultorias de segurança na Base de Dados de Consultoria do GitHub

1. Navegue até a [Base de Dados de Consultoria do GitHub](https://github.com/advisories).
2. Digite ou cole `follow-redirects` na caixa de pesquisa de consultorias.
3. Clique em qualquer uma das consultorias encontradas para ver mais informações.
4. Você verá os pacotes, impacto, patches, soluções alternativas e referências para a consultoria.

Observe a longa lista de consultorias para nossa dependência! Isso pode parecer assustador, mas na verdade é uma coisa boa. Significa que nossa dependência está sendo ativamente mantida e patches estão sendo disponibilizados para remover a vulnerabilidade. Se tivéssemos alertas do Dependabot habilitados, poderíamos receber alertas quando precisássemos atualizar uma dependência e agir prontamente para protegê-la.

Vamos habilitar alertas do Dependabot em nosso repositório!

### :keyboard: Atividade 2.2: Habilitar alertas do Dependabot

1. Navegue até a aba **Settings**.
2. Exiba as configurações para **Advanced Security**.
3. Habilite **Dependabot alerts**.
4. **Aguarde cerca de 60 segundos para o Dependabot verificar se há alertas.**
5. Navegue até a aba **Security**.
6. Em "Vulnerability alerts" na barra lateral, selecione **Dependabot** para visualizar uma lista dos alertas do Dependabot para a branch padrão.

O Dependabot nos alertou sobre vulnerabilidades nas dependências que usamos. Também podemos usar o Dependabot para nos ajudar a resolver essas vulnerabilidades criando pull requests para atualizar a dependência para uma versão segura.

Vamos ver como isso funcionaria usando o Dependabot para criar um pull request para um dos alertas!

### :keyboard: Atividade 2.3: Criar um pull request com base em um alerta do Dependabot

1. Na lista de alertas do Dependabot, clique em "Prototype Pollution in minimist" para exibir mais informações.
2. Clique no botão **Create Dependabot security update** para criar um pull request para atualizar a dependência. Isso pode levar até 2 minutos.
3. Quando o pull request estiver aberto, a página de alerta será atualizada para mostrar um botão **Review security update**.
4. Clique no botão **Review security update** para exibir o pull request.
   - Você pode visualizar o pull request e a aba **Files changed** para revisar a atualização.
5. Navegue de volta para a aba **Conversation** e faça o merge do pull request.

Espere cerca de 20 segundos e então atualize esta página (a página onde você está seguindo as instruções). [GitHub Actions](https://docs.github.com/en/actions) será atualizado automaticamente para exibir o próximo passo.
