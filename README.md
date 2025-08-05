# 3D-game-engine
Made by Louann Naccache last year. Authorship is reserved to Louann Naccache
Made last year. If you're motivated to create graphical games from scratch this is for you !
J'avais terminé ma Seconde lors de la création de ce projet. J'ai étudié méthodiquement,
le mouvement des objects dans le champs de vision lors qu'ils sont immobiles et que 
l'obsvateur est en mouvement et vice-versa. J'avais remarqué que lorsqu'on s'éloigne de l'object 
celui-ci devient de plus en plus haut dans le champs de vision jusqu'à arriver à l'horizon, et petit.
J'ai aussi remarqué que lorsque l'on tourne vers un objet, celui-ci balaye seulement le champs de vision sans
changer de taille...
Je pensais alors faire plusieurs formule pour chaque mouvement, et les rotations.
Cependant, j'ai vite compris que la vision n'est pas comme un écran (ou cadre de tableau vide) qui
affiche ce qu'il voit. C'est en fait, un point qui nous sert de capteur visuelle.
Alors tout a changé depuis là. J'ai alors compris que pour calculer la position d'un objet, dans
le champs de vision, il falait savoir sa distance par rapport au centre (pic) du champs visuelle.
C'est-à-dire le distance 2D entre l'obsvateur et l'objet (sachant que l'object est un point,
autant que l'obsvateur). Pour calculer cette dernière, il faut prendre en compte la distance 3D entre
l'observateur (qui est un point), et l'object, c'est-à-dire cette distance mais mesuré que dans la direction
de l'observateur (tout droit jusqu'à arriver au même niveau que l'objet ou le point. C'est un peu comme la distance
que parcours une onde bien répartie pour atteindre l'objet ou le point. De même, il faut y ajouter la simple distance entre,
l'observateur et le point ou l'objet. Ainsi on y construit un triangle.
Puis il sufit d'appliquer de la trigonométrie (niveau 3e) pour retrouver la
distance voulu à partir des deux autres.
