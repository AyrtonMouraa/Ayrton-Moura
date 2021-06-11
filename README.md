# Ayrton Moura 🖥️

 **Welcome to my profile 👋**

My name is Ayrton Moura, I'm from Brazil 🇧🇷.  I'm  A Computer Networking Technician, that has been working as an intern in TI support since January 2021.

I am passionate about solving Cyber Security and learning. Always open to new challenges and ready to face changes. 

 

###   "Acredito verdadeiramente que para se defender é preciso conhecer o inimigo e as ameaças que nos cercam. Aqui eu compartilho tudo que aprendo no campo de batalha." 🔥
 

-  🌎 From PE Pernambuco my Country
-  👨‍🎓  Finishing College in Computer Networks 
-  🖥️ Pentest 

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=AyrtonCyberSec&show_icons=true&theme=radical)

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: AyrtonCyberSec
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
