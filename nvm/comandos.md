# 🔧 Comandos NVM

### Para ver qual é a versão do node
```bash
node -- version
```

### Para ver qual é a versão do npm
```bash
npm --version
```

### Lista as versões disponíveis remotamente para download.
```js
nvm ls-remote
```

### Lista as versões já instaladas
```js
nvm ls
// ou
nvm list
```


### Para fazer o download de uma versão especifica, podemos usar o comando.
```js
nvm install <versão>
nvm install v10.21.0
nvm install v18.7.0
```

### Para utilizar uma versão especifica podemos utilizar o comando.
```js
nvm use <versão>
nvm use v10.21.0
nvm use 14.20.0
```

**OBS**: Esse processo já edita o arquivo ```~/.bashrc``` colocando a referencia do nvm. Caso o processo não modifique coloque a seguinte instrução no final do arquivo ```.bashrc```


### 
```js
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```
Após essa alteração, precisamos fazer o carregamento desse arquivo com o seguinte comando.


### 
```js
source ~/.bashrc
```

Para poder ver qual a versão do NVM podemos executar o seguinte comando. 

### 
```js
nvm --version
```
Podemos ter uma versão padrão do node em nossa maquina. para saber qual é q versão padrão no NVM podemos utilizar

### 
```js
nvm use default
```

Para alterar a versão padrão do node no NVM podemos utilizar
### 
```js
nvm alias default <Versão>
nvm alias default 18.7.0
```

### **Porque não usar Docker?**

Atualmente a moda é usar o Docker, e realmente é muito bom, facilitam as coisas, porém você pode pensar, porque então não usá-lo para manter versões diferentes do Node.JS na máquina? Bom, mesmo o Docker facilitando muito as coisas, o NVM consegue nesse cenário facilitar mais ainda.

Com o Docker, teríamos que executar um container para cada versão diferente do Node.JS, fora o tamanho das imagens que teremos que fazer o download e deixar na nossa máquina. E particularmente acho bem mais simples usar o comando ```nvm ls-remote``` para listar todas as versões disponíveis e ```use v13.5.0``` para usar uma determinada versão.

