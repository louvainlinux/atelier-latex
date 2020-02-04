Atelier LaTeX
----------

Conférence LaTeX du [Louvain-li-Nux](https://louvainlinux.org).

Plus d'infos sur <https://louvainlinux.org/activites/atelier-latex>.

## Compiler les slides

À la racine du reposetory, exécutez: `make clean all`, le nouveau fichier `main.pdf` devrait être accessible dans le dossier `build_latex`.

Les options par défaut passée à `latexmk` sont `-pdf -lualatex -cd -silent`, vous pouvez en ajouter en définissant `LATEX_FLAGS` dans votre environnement ou en passant sa valeur à `make`, par exemple: `make LATEX_FLAGS=-verbose`.

Vous pouvez aussi ajouter des instructions bash à la fin de la commande, en définissant `BASH_POSTPROCESSING` dans votre environnement ou en passant sa valeur à `make`. Les variables spéciales sont accessibles, par exemple pour rediriger l'output complète vers un logfile pour chaque fichier compilé: `make LATEX_OPT=-verbose BASH_POSTPROCESSING=2>&1 1>$(@D)/out.log`, ou encore pour supprimer tout logs de `latexmk`: `make BASH_POSTPROCESSING=2>/dev/null 1>/dev/null`.

## Contribuer

N'hésitez pas à proposer des amélioration à ces slides (via pull requests) !

## Déployer des changements

(Information destinée aux membre du Louvain-li-Nux)

Faire tous les développements sur la branche devel. Le modifications sont
prêtes (typiquement, juste avant l'atelier), créer une pull request vers la
branche master et la merger. La version qui est sur master est celle qui est
publiée sur GitHub Pages
(<https://louvainlinux.github.io/atelier-latex/src/build_latex/main.pdf>), vers
laquelle les liens du site <https://louvainlinux.org> pointent.

## License

La présentation est disponible sous license `CC-BY 4.0`.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>
<br />This work is licensed under a
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

