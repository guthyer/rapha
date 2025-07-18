# Projeto: "Vozes das Cores" - Desenvolvendo um Site com Python

O objetivo deste projeto é criar um site informativo sobre uma das campanhas "Cores do Mês" (como Outubro Rosa, Novembro Azul, etc.). O estudante escolherá uma cor/causa e usará Python para gerar as páginas do site de forma automatizada. Ao final, o site será publicado gratuitamente na web usando o GitHub Pages.

---

## 🛠 Tecnologias Utilizadas

- **Python**: Para a lógica de *back-end* (geração do site)
- **HTML5**: Para a estrutura do site
- **CSS3**: Para a estilização e design
- **GitHub Pages**: Para publicação gratuita do site

---

## 📌 Passo a Passo do Projeto

### 🔍 Fase 1: Pesquisa e Planejamento

1. **Escolha da Cor/Causa**
   - Janeiro Branco: Saúde Mental
   - Março Lilás: Conscientização sobre o Câncer de Colo do Útero
   - Setembro Amarelo: Prevenção ao Suicídio
   - Outubro Rosa: Conscientização sobre o Câncer de Mama
   - Novembro Azul: Saúde do Homem

2. **Defina o Conteúdo**
   - O que é a campanha?
   - Qual a importância da causa?
   - Dados e estatísticas
   - Como ajudar ou se prevenir?
   - Fontes e links úteis

3. **Desenhe o Wireframe**
   - Estrutura visual da página em papel ou ferramenta online.

---

### 💻 Fase 2: Configuração do Ambiente

- Instale o Python (https://www.python.org)
- Use um editor como **VS Code** ou **Sublime Text**
- Estrutura de pastas recomendada:

/projeto-cores/
├── gerador_site.py
├── template.html
├── style.css
├── conteudo.txt
└── index.html
---

### 🎨 Fase 3: Desenvolvimento Front-End

- **template.html**: HTML com placeholders (`{{TITULO}}`, `{{CONTEUDO}}`)
- **style.css**: Estilo do site com a cor da campanha

---

### 🧠 Fase 4: Lógica Python (Back-End)

Script `gerador_site.py`:

```python
# Abre e lê o arquivo de template
with open('template.html', 'r', encoding='utf-8') as file:
    template = file.read()

# Abre e lê o arquivo de conteúdo
with open('conteudo.txt', 'r', encoding='utf-8') as file:
    conteudo = file.read()

# Define os valores para substituir no template
titulo_pagina = "Março Lilás - Mulheres em Foco"
titulo_cabecalho = "Março Lilás: Pela Dignidade e Direitos das Mulheres"

# Substitui os marcadores pelos conteúdos
html_final = template.replace('{{TITULO_PAGINA}}', titulo_pagina)
html_final = html_final.replace('{{TITULO_CABECALHO}}', titulo_cabecalho)
html_final = html_final.replace('{{CONTEUDO}}', conteudo)

# Cria e escreve o arquivo final index.html
with open('index.html', 'w', encoding='utf-8') as file:
    file.write(html_final)

print("Site gerado com sucesso! Abra o arquivo 'index.html' no seu navegador.")

5. Script Python (gerador_site.py)
# Abre e lê o arquivo de template
with open('template.html', 'r', encoding='utf-8') as file:
    template = file.read()

# Abre e lê o arquivo de conteúdo
with open('conteudo.txt', 'r', encoding='utf-8') as file:
    conteudo = file.read()

# Define os valores para substituir no template
titulo_pagina = "Março Lilás - Mulheres em Foco"
titulo_cabecalho = "Março Lilás: Pela Dignidade e Direitos das Mulheres"

# Substitui os marcadores pelos conteúdos
html_final = template.replace('{{TITULO_PAGINA}}', titulo_pagina)
html_final = html_final.replace('{{TITULO_CABECALHO}}', titulo_cabecalho)
html_final = html_final.replace('{{CONTEUDO}}', conteudo)

# Cria e escreve o arquivo final index.html
with open('index.html', 'w', encoding='utf-8') as file:
    file.write(html_final)

print("Site gerado com sucesso! Abra o arquivo 'index.html' no seu navegador.")
