# Guia de Lançamento no GitHub Pages

Este documento fornece instruções passo-a-passo para lançar o VukaSport no GitHub Pages.

## Pré-requisitos

- Conta GitHub (crie uma em https://github.com/signup)
- Git instalado no seu computador
- Conhecimento básico de linha de comando

## Passo 1: Criar um Repositório no GitHub

1. **Aceda a GitHub**
   - Visite https://github.com
   - Faça login na sua conta

2. **Crie um novo repositório**
   - Clique no ícone "+" no canto superior direito
   - Selecione "New repository"

3. **Configure o repositório**
   - Nome: `vukasport` (ou `vukasport-app`)
   - Descrição: "VukaSport - Acompanhe todos os resultados desportivos em tempo real"
   - Visibilidade: **Public** (importante para GitHub Pages)
   - Não inicialize com README (vamos usar o nosso)

4. **Clique em "Create repository"**

## Passo 2: Preparar o Projeto Localmente

1. **Abra o terminal/command prompt**

2. **Clone o repositório vazio**
   ```bash
   git clone https://github.com/seu-usuario/vukasport.git
   cd vukasport
   ```

3. **Copie os arquivos do projeto**
   - Copie todos os arquivos do VukaSport para este diretório
   - Certifique-se de que `index.html` está na raiz

4. **Verifique a estrutura**
   ```
   vukasport/
   ├── index.html
   ├── manifest.json
   ├── robots.txt
   ├── sitemap.xml
   ├── README.md
   ├── INSTALLATION.md
   ├── CONTRIBUTING.md
   ├── LICENSE
   ├── .gitignore
   ├── app-icon.png
   └── assets/
       ├── index-BREznCSF.css
       └── index-B7_SQaDH.js
   ```

## Passo 3: Fazer Commit e Push

1. **Adicione todos os arquivos**
   ```bash
   git add .
   ```

2. **Crie um commit inicial**
   ```bash
   git commit -m "Initial commit: VukaSport landing page"
   ```

3. **Faça push para o GitHub**
   ```bash
   git push -u origin main
   ```

## Passo 4: Ativar GitHub Pages

1. **Vá para as configurações do repositório**
   - Abra https://github.com/seu-usuario/vukasport
   - Clique em "Settings"

2. **Navegue para GitHub Pages**
   - No menu esquerdo, clique em "Pages"

3. **Configure a fonte**
   - Em "Source", selecione "Deploy from a branch"
   - Em "Branch", selecione "main" e "/root"
   - Clique em "Save"

4. **Aguarde a publicação**
   - GitHub Pages levará alguns minutos para publicar
   - Você receberá um link como: `https://seu-usuario.github.io/vukasport`

## Passo 5: Verificar o Site

1. **Aceda ao seu site**
   - Visite: `https://seu-usuario.github.io/vukasport`
   - Verifique se tudo está funcionando corretamente

2. **Teste as funcionalidades**
   - Verifique se os links de download funcionam
   - Teste a responsividade em dispositivos móveis
   - Verifique o SEO no Google Search Console

## Passo 6: Configurar Domínio Personalizado (Opcional)

Se deseja usar um domínio personalizado como `vukasport.com`:

1. **Compre um domínio**
   - Use serviços como Namecheap, GoDaddy, etc.

2. **Configure os registos DNS**
   - Adicione registos CNAME ou A apontando para GitHub Pages
   - Consulte a documentação do seu registador

3. **Configure no GitHub**
   - Vá para Settings > Pages
   - Em "Custom domain", digite seu domínio
   - Clique em "Save"

4. **Aguarde a propagação**
   - Pode levar até 24 horas para propagar

## Passo 7: Configurar HTTPS

1. **GitHub Pages ativa HTTPS automaticamente**
   - Aguarde alguns minutos após configurar o domínio
   - Um certificado SSL será gerado automaticamente

2. **Force HTTPS**
   - Em Settings > Pages
   - Ative "Enforce HTTPS"

## Atualizações Futuras

### Fazer Alterações

1. **Edite os arquivos localmente**
   ```bash
   # Faça suas alterações
   ```

2. **Commit e push**
   ```bash
   git add .
   git commit -m "Descrição das alterações"
   git push
   ```

3. **GitHub Pages atualizará automaticamente**
   - Leva alguns minutos

### Atualizar a Aplicação

1. **Atualize o link de download**
   - Edite `index.html`
   - Atualize o link do Google Drive se necessário

2. **Atualize a versão**
   - Edite `manifest.json`
   - Atualize `softwareVersion` em `index.html`

3. **Commit e push**
   ```bash
   git add .
   git commit -m "Update to version X.X"
   git push
   ```

## Otimizações Recomendadas

### 1. Submeter ao Google Search Console

1. Visite https://search.google.com/search-console
2. Adicione sua propriedade
3. Submeta o `sitemap.xml`
4. Verifique a indexação

### 2. Configurar Analytics

1. Crie uma conta em Google Analytics
2. Adicione o código de rastreamento ao `index.html`
3. Monitore o tráfego

### 3. Otimizar Performance

1. Comprima imagens
2. Minifique CSS/JS
3. Use um CDN se necessário

## Solução de Problemas

### Problema: Site não aparece após push

**Solução:**
1. Aguarde 5-10 minutos
2. Verifique se GitHub Pages está ativado
3. Verifique se `index.html` está na raiz
4. Limpe o cache do navegador

### Problema: Estilos não aparecem

**Solução:**
1. Verifique se `manifest.json` está correto
2. Verifique os caminhos dos arquivos CSS/JS
3. Abra o DevTools (F12) para ver erros

### Problema: Links de download não funcionam

**Solução:**
1. Verifique se o link do Google Drive está correto
2. Teste o link em uma aba privada
3. Verifique as permissões do arquivo

## Comandos Git Úteis

```bash
# Ver status
git status

# Ver histórico de commits
git log

# Reverter para um commit anterior
git revert <commit-hash>

# Criar uma nova branch
git checkout -b feature/nova-funcionalidade

# Fazer merge de uma branch
git merge feature/nova-funcionalidade
```

## Recursos Úteis

- [Documentação GitHub Pages](https://docs.github.com/en/pages)
- [Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
- [Markdown Guide](https://www.markdownguide.org/)

## Suporte

Se encontrar problemas:

📧 **Email:** visinovatech@gmail.com

---

**Versão:** 1.0  
**Última Atualização:** 28 de Fevereiro de 2026
