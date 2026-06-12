# 💕 Surpresa Romântica - Dia dos Namorados

Um site minimalista e elegante com slider animado e efeito de fundo estilo "velocidade da luz".

## 📁 Estrutura do Projeto

```
surprise-valentines/
├── index.html       # Estrutura do site
├── styles.css       # Estilos e animações
├── script.js        # Interatividade e efeitos
├── README.md        # Este arquivo
└── assets/          # (opcional) Pasta para imagens e música
    ├── images/
    └── music/
```

## 🚀 Como Usar

### 1. **Testar Localmente**
Abra o arquivo `index.html` no seu navegador (ou use Live Server no VS Code).

### 2. **Adicionar Imagens**
Crie uma pasta `assets/images/` e adicione suas imagens. Depois edite o `index.html`:

```html
<div class="slide" data-index="0">
    <div class="slide-content">
        <img src="assets/images/foto1.jpg" alt="Foto nossa">
        <h2>Olá, meu amor ❤️</h2>
        <p>Você merecia algo especial</p>
    </div>
</div>
```

**CSS para a imagem** (adicione ao `styles.css`):
```css
.slide-content img {
    width: 100%;
    max-width: 400px;
    height: auto;
    border-radius: 15px;
    margin-bottom: 20px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}
```

### 3. **Adicionar Música**
Crie a pasta `assets/music/` e adicione seu arquivo de música (MP3 ou OGG).

No `index.html`, procure por:
```html
<audio id="bgMusic" loop>
    <!-- Adicione a música aqui -->
</audio>
```

E mude para:
```html
<audio id="bgMusic" loop>
    <source src="assets/music/sua-musica.mp3" type="audio/mpeg">
</audio>
```

---

## 📝 Comandos Git Básicos

### **Primeira vez: Conectar ao GitHub**

1. Crie um repositório novo no GitHub:
   - Vá para https://github.com/new
   - Nome: `surprise-valentines`
   - Descrição: "Surpresa romântica para dia dos namorados"
   - Deixe como **Private** se quiser
   - Clique em **Create repository**

2. No seu terminal (dentro da pasta `surprise-valentines`):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@example.com"

git add .
git commit -m "Initial commit: setup básico"

git branch -M main
git remote add origin https://github.com/SEU-USUARIO/surprise-valentines.git
git push -u origin main
```

### **Depois: Cada vez que você fizer mudanças**

```bash
# Ver o que mudou
git status

# Adicionar tudo
git add .

# Commit (mensagem descritiva)
git commit -m "Descrição da mudança"

# Enviar para GitHub
git push
```

**Exemplos de boas mensagens:**
```bash
git commit -m "Adiciona imagens dos slides"
git commit -m "Muda cor do fundo"
git commit -m "Corrige efeito de partículas"
git commit -m "Adiciona música de fundo"
```

---

## 🌐 Deploy no Vercel

### **Passo 1: Conectar Vercel ao GitHub**
1. Vá para https://vercel.com
2. Clique em **Sign Up** ou **Log In** com GitHub
3. Clique em **New Project**
4. Selecione seu repositório `surprise-valentines`
5. Clique em **Import**

### **Passo 2: Configurar**
- **Framework Preset**: Selecione **Other** (é HTML puro)
- **Build Command**: Deixe em branco
- **Output Directory**: Deixe em branco
- Clique em **Deploy**

### **Pronto!** ✅
Seu site estará rodando em uma URL tipo:
```
https://surprise-valentines.vercel.app
```

---

## 🎨 Personalizações Rápidas

### **Mudar as cores**
No `styles.css`, procure por:
```css
background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
```

Mude para cores que quiser. Algumas sugestões:
- **Rosa**: `#ff1654` a `#ff69b4`
- **Roxo**: `#9b59b6` a `#3b0e54`
- **Azul**: `#1e3a8a` a `#0369a1`

### **Mudar a velocidade do efeito de fundo**
No `script.js`, procure por:
```javascript
this.speedZ = Math.random() * 4 + 2;
```

Aumentar o número = mais rápido. Diminuir = mais lento.

### **Auto-avançar slides**
No `script.js`, descomente (remova `/*` e `*/`):
```javascript
setInterval(() => {
    nextSlide();
}, 8000); // Muda a cada 8 segundos
```

---

## ⌨️ Atalhos

| Ação | Tecla |
|------|-------|
| Próximo slide | Seta direita (→) |
| Slide anterior | Seta esquerda (←) |
| Clicar nos pontos | Vai para aquele slide |

---

## 💡 Próximas Ideias (Para Depois)

- [ ] Adicionar um contador regressivo
- [ ] Efeito de confete ao passar entre slides
- [ ] Formulário para adicionar mais mensagens
- [ ] Galeria com múltiplas fotos por slide
- [ ] Modo escuro/claro

---

## 🐛 Dúvidas Comuns

**P: As imagens não aparecem**
- Verifique se o caminho está certo (relativo a `index.html`)
- Tente usar URLs se estiver testando (ex: URL de imagem do Google)

**P: A música não toca**
- Alguns navegadores pedem permissão de áudio
- Tente clicar no botão 🎵 primeiro

**P: Quer adicionar vídeo no lugar de foto?**
- Troque `<img>` por `<video>`:
```html
<video width="400" controls>
    <source src="assets/video.mp4" type="video/mp4">
</video>
```

---

## 📞 Pronto para evoluir?
Quando quiser adicionar:
- Formulários interativos
- Mais animações
- Integrar banco de dados
- Compartilhamento em redes sociais

Me chama! 🚀

---

**Feito com ❤️ para sua surpresa perfeita**