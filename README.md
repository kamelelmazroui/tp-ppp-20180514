# TP Markdown (partie 2)

## Le format Markdown

Markdown est un langage de balisage léger créé par John Gruber en
2004. Son but est d’offrir une syntaxe facile à lire et à écrire.

Un document rédigé en Markdown peut être converti facilement en PDF, ODT, DOCX, etc ...

La syntaxe Markdown peut-être retrouvée ici :
 
 - [fr.wikipedia.org/wiki/Markdown](https://fr.wikipedia.org/wiki/Markdown)
 - [cheatsheet online @ GitHub](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

## Le travail du jour 

Créér une base de (joli) CV au format ~~LaTex (même si [moderncv](https://ctan.org/pkg/moderncv) est super)~~ Markdown pour l'afficher sur votre site web perso ou pour le diffuser ( si vous cherchez un job d'été par exemple :monkey_face: ).

### Structure du CV 

1. Vous
2. Votre fonction 
3. Votre expérience pro (si vous en avez)
4. Vos contributions, vos réalisations, ...
5. Votre parcours (scolaire)
6. Vos centres d'intérêt et tout le reste 

> Rappel : on ne dépasse pas 1 page hein :)

### Et après ?

On peut utiliser [pandoc](https://github.com/jgm/pandoc/releases) pour transformer son document Markdown et le convertir facilement.

Exemple :

```
pandoc --standalone --from markdown --to docx -o mon_cv.docx mon_cv.md
pandoc --standalone --from markdown --to html -o index.html mon_cv.md
``` 

Exemple façon LaTex : 

```
pandoc mon_cv.md --pdf-engine=xelatex -o mon_cv.pdf -V papersize:a4paper
```

### C'est moche ...

Oui, mais on peut faire mieux. 

> NB: Normalement, vous avez des notions en CSS.

Le fichier `mon_cv-style.md` + un fichier `style.css` et c'est assez magique.

```
pandoc --standalone -c style.css --from markdown --to html -o index.html mon_cv-style.md
```

Alors, convaincus ? :monkey:

## À vous 

Fichier .md (+ éventuellement style.css) à me remettre pour notre dernière séance au plus tard ! (via Slack ou email)
