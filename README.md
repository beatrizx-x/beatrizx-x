
<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=180&section=header&text=Ana%20Beatriz&fontSize=60&fontAlignY=40&animation=twinkling&theme=radical)

## ✨ Bem-vindo(a) ao meu perfil! ✨

<p align="center">
  <b>Front-end Developer em formação </b> e entusiasta de <b> UX/UI Design</b>.<br>
  Transformando código em experiências visuais incríveis.
</p>

---

### 🛠️ No que estou trabalhando:

<section> 
<ul>
  <li>
📚 Estudando Análise e Desenvolvimento de Sistemas
  </li>
</ul><ul>
  <li>
  💻 Aprimorando Hardskills no Entra21             
  </li>
</ul><ul>
  <li>
  🧪 Explorando a união de UX Design com desenvolvimento web
  </li>
</ul>
</section>
<br>

## 🚀 Hardskills

<img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white" /> <img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white" /> <img src="https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black" /> <img src="https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white" /> <img src="https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white" />

<br>
<br>

| 🐱  | 📊  |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/791d5059-c9cc-466a-8faf-435153be4fd9" width="280px"> | <img src="https://github-readme-streak-stats.herokuapp.com/?user=beatrizx-x&theme=radical&hide_border=true" /> |

<br>

---
*“Transformando ideias em interfaces e café em código🧋”* 
![Cafe](https://img.shields.io/badge/-Coffee%20Time-6F4E37?style=flat-square&logo=coffeescript&logoColor=white)

</div>

name: Generate Snake

on:
  schedule: # Executa a cada 24 horas
    - cron: "0 */24 * * *"
  workflow_dispatch: # Permite rodar manualmente

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Generate Snake Files
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Push Snake to Output Branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}






