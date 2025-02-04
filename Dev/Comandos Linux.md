#DevOps 
[[Cloud]]
### 📂 **Gerenciamento de Arquivos e Diretórios**

- `ls` – Lista arquivos e diretórios
- `cd [diretório]` – Navega entre diretórios
- `pwd` – Mostra o caminho do diretório atual
- `mkdir [nome]` – Cria um diretório
- `rm [arquivo]` – Remove um arquivo
- `rm -r [diretório]` – Remove diretório e seu conteúdo
- `cp [origem] [destino]` – Copia arquivos/diretórios
- `mv [origem] [destino]` – Move/renomeia arquivos

### 🔍 **Visualização de Arquivos**

- `cat [arquivo]` – Exibe o conteúdo de um arquivo
- `tac [arquivo]` – Exibe o conteúdo de trás para frente
- `less [arquivo]` – Permite visualizar o conteúdo paginado
- `head -n [num] [arquivo]` – Exibe as primeiras linhas
- `tail -n [num] [arquivo]` – Exibe as últimas linhas

### 🛠 **Gerenciamento de Processos**

- `ps aux` – Lista processos em execução
- `top` – Exibe processos em tempo real
- `kill [PID]` – Encerra um processo específico
- `pkill [nome]` – Mata um processo pelo nome

### 🔧 **Permissões e Usuários**

- `chmod [permissão] [arquivo]` – Altera permissões de arquivos
- `chown [usuário]:[grupo] [arquivo]` – Muda o dono de um arquivo
- `sudo [comando]` – Executa um comando como superusuário
- `useradd [nome]` – Cria um novo usuário
- `passwd [usuário]` – Altera senha do usuário

### 📦 **Gerenciamento de Pacotes**

- **Debian/Ubuntu:**
    - `apt update` – Atualiza repositórios
    - `apt install [pacote]` – Instala um pacote
    - `apt remove [pacote]` – Remove um pacote
- **CentOS/RHEL:**
    - `yum install [pacote]`
    - `yum remove [pacote]`

### 🌍 **Rede**

- `ping [host]` – Testa conexão com um servidor
- `curl [URL]` – Faz requisições HTTP
- `wget [URL]` – Baixa arquivos da internet
- `ifconfig` ou `ip addr` – Exibe informações de rede
- `netstat -tulnp` – Mostra conexões ativas

### 🔍 **Busca e Filtros**

- `grep [padrão] [arquivo]` – Busca por texto em arquivos
- `find [diretório] -name [padrão]` – Procura arquivos
- `awk '{print $1}' [arquivo]` – Filtra colunas
- `sed 's/original/novo/g' [arquivo]` – Substitui texto

### ⏳ **Outros**

- `history` – Mostra o histórico de comandos
- `clear` – Limpa o terminal
- `exit` – Sai da sessão