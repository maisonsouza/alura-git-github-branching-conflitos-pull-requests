# Curso de Git e Github: Estratégias de ramificação, Conflitos e Pull Requests

![](https://www.alura.com.br/assets/api/share/curso-git-github-branching-conflitos-pull-requests.png)

> Aula01 - Github e OpenSource
- O que são e como utilizar ***issues***
- Que as *issues* podem ser utilizadas para vários propósitos
 - Reportar problemas
 - Sugerir melhorias
 - Solicitar novas funcionalidades
 - Organizar qualquer coisa que faça sentido para o projeto
 - Etc
- O que são ***pull requests***
- Como unir vários *commits* em um, utilizando o comando `git rebase -i`

>Aula02 - Controle avançado de conflitos
- Que o comando `git cherry-pick` pode trazer um *commit* específico para a *branch* atual;
- Como encontrar o *commit* em que determinada alteração foi aplicada, utilizando o `git bisect`;
- Como encontrar o responsável por determinada linha ou bloco de código, utilizando o `git blame`;
- Que jamais devemos apontar um culpado por determinado *bug*. Uma equipe deve ser unida e se ajudar;
- Que o comando `git show {hash}` mostra todas as alterações aplicadas pelo *commit* com o *hash* informado.

> Aula03 - Estratégias de branching

- Que é uma convenção bem seguida que a *branch* `master` tenha apenas os *commits* prontos para ir para produção;
- Que não é interessante realizar trabalho e *commitar* diretamente na *branch* `master`;
- Como remover uma *branch*:
 - `git branch -d {nome_branch}` remove uma *branch* que já tem seu trabalho unido à *branch* atual;
 - `git branch -D {nome_branch}` remove uma *branch* mesmo que os *commits* desta *branch* ainda não estejam na *branch* atual, ou seja, força a remoção;
- Um pouco do processo chamado de ***Git Flow***:
 - Entendemos que o estado do código representado pela *branch* `master` deve ser o mesmo que estará em produção
 - Vimos que deve haver uma *branch* de desenvolvimento (comumente chamado de `develop`), onde todas as funcionalidades e correções devem ser muito bem testadas antes de ir para produção (`master`)
 - Vimos que cada funcionalidade deve ser feita em uma *branch* separada, e que é comum que esta *branch* tenha `feature/` como prefixo
 - Aprendemos também que *bugs* normalmente são corrigidos em *branches* separadas, com o prefixo `hotfix/`
 - Além disso, *branches* específicas para cada *release* são criadas para realizar os testes e correções de *bugs* específicos
