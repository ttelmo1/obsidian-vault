#DevOps 
### **Windows**:

1. **Abra o PowerShell** ou o Prompt de Comando.
2. Execute o comando:
    
    `ssh-keygen -t rsa -b 4096 -C "seu_email@example.com"`
    
3. Pressione **Enter** para aceitar o local padrão (`C:\Users\SeuUsuário\.ssh\id_rsa`) ou especifique um caminho personalizado.
4. Se desejar, defina uma senha para a chave (ou pressione **Enter** para continuar sem senha).
5. A chave pública será salva como `id_rsa.pub` e a privada como `id_rsa`.

### **Linux**:

6. **Abra o terminal**.
7. Digite o comando:
    
    `ssh-keygen -t rsa -b 4096 -C "seu_email@example.com"`
    
8. Escolha um diretório para salvar (padrão: `~/.ssh/id_rsa`) ou pressione **Enter** para aceitar.
9. Defina uma senha para a chave (ou pressione **Enter** para continuar sem senha).
10. A chave pública estará no arquivo `id_rsa.pub`, e a privada em `id_rsa`.

### **Adicionando a chave ao SSH-Agent (Opcional)**

Para facilitar o uso da chave, adicione-a ao SSH-Agent:

- **Windows**:
    
    `Start-Service ssh-agent ssh-add $env:USERPROFILE\.ssh\id_rsa`
    
- **Linux**:
    

    `eval "$(ssh-agent -s)" ssh-add ~/.ssh/id_rsa`