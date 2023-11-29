# Redirecionamento HTTP para HTTPS

Este conjunto de regras de reescrita para o servidor Apache é projetado para realizar o redirecionamento de requisições HTTP para HTTPS. Isso é útil para garantir uma conexão segura, direcionando automaticamente os visitantes para a versão segura do seu site.

### Configuração

1. **Ative o Módulo de Reescrita:**

   Certifique-se de que o módulo de reescrita do Apache esteja ativado. Você pode fazer isso executando o seguinte comando:

   ```bash
   a2enmod rewrite
   ```

   E, em seguida, reinicie o Apache:

   ```bash
   systemctl restart apache2
   ```

2. **Integração no seu Arquivo de Configuração do Apache ou em um arquivo .htaccess:**

   Adicione as seguintes linhas ao seu arquivo de configuração do Apache ou a um arquivo `.htaccess` no diretório desejado:

   ```apache
   RewriteEngine On
   RewriteCond %{HTTPS} off
   RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
   ```

3. **Entendendo as Regras:**

   - `RewriteEngine On`: Ativa o mecanismo de reescrita do Apache.

   - `RewriteCond %{HTTPS} off`: Verifica se a conexão não está usando HTTPS.

   - `RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]`: Redireciona a requisição para a versão HTTPS do mesmo URL, adicionando `https://` ao início. O código de resposta `301` indica um redirecionamento permanente.

### Notas

- **Certificado SSL:**
  Certifique-se de ter um certificado SSL instalado no seu servidor para garantir que a transição para HTTPS seja segura.

- **Configuração Adicional:**
  Essas regras são um exemplo básico. Dependendo da sua configuração específica, você pode precisar ajustar as regras de reescrita.

### Contribuições

Se você tiver sugestões ou melhorias, sinta-se à vontade para abrir um problema ou enviar um pedido de recebimento.

Mantenha seu site seguro!
