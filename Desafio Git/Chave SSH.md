# Chave SSH



#### Chaves já existentes

- Para listar as existentes, executar o comando: `ls -al ~/.ssh`

  

#### Gerar uma nova chave

- Para criar uma chave ed25519, executar: `ssh-keygen -t ed25519 -C "your_email@example.com"`

- Para criar uma chave rsa, executar: `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

  

#### Adicionar chave privada no ssh-agent

- Rodar o ssh-agent: `eval $(ssh-agent -s)`

- Incluir a chave privada: `ssh-add ~/.ssh/id_ed25519`

  

#### Copiar chave pública

- **No Windows:** `clip < ~/.ssh/id_ed25519.pub`. (Automaticamente o conteúdo da sua chave pública será copiado para a área de transferência.)

  

#### Adicionar chave no Github

- Abra o Github e vá no ícone de perfil > Settings, no canto superior direito.

- Na barra lateral de configurações do usuário, clique em "SSH and GPG keys".

- Clique no botão "New SSH key"

- No campo "Título", adicione um rótulo descritivo para a nova chave. Por exemplo, se estiver usando seu computador pessoal, você pode chamar essa chave de "Computador pessoal".

- Cole a chave pública que está na área de transferência no campo "Chave".

- Clique em "Add SSH key" e pronto!

  

#### Testando a conexão SSH

- Executar o seguinte comando: `ssh -T git@github.com`
- Aguardar as mensagens. Digitar "yes" para continuar.
- Verifique se a mensagem resultante contém seu nome de usuário e o sucesso da sua autenticação.
