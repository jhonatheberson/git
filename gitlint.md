#cria node.js packjson
  *npm init*
#cria arquivo de configuração do commitlint
  *echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js"*
#reciso ter repositorio do git ja na pasta e lincado para comando a seguir
  *npm install husky -D --save* ->  **'D' é de desenvolvimento '--save' save onde esta sendo executado**
#instala commitizen
  *npm install commitizen -D --save* -> **uma template para commit via terminal**
#configura o commitizen no seu projeto
  *npx commitizen init cz-conventional-changelog --save-dev --save-exact*
#dispara o commitizen
  *"husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS",
      "prepare-commit-msg": "exec < /dev/tty && git cz --hook || true"
    }
  },* -> **"commit": "git-cz"**
