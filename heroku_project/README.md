![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/hlogo.png)

## tuto deploiement heroku

apres avoir crée mon app avec django

# Installer heroku avec la commande :
$ sudo snap install heroku --classic

# connecte aux compte heroku avec la commande :
$ heroku login

j'appuie sur un touche afin d'ouvrir mon naviguateur et accepter la connection a mon compte

![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/herokulogin.png)

# creation de l'app en donnant un nom avec la commande :

$ heroku create testederherokuapptuto

ou (testederherokuapptuto) et le nom que je choisit sinon

$ heroku create 

pour laisser heroku donner un nom

![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/herokucreateapp.png)

# creation d'un fichier runtimes.txt a la racine du projet
# noter dedans la version de python utiliser pour le projet trouver la version avec la commande :
$ python -V
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/runtimes.png)

noter dans le fichier la version avec python en miniscule et un tirer du six entre python et la version 
# installation de gunicorn avec la commande :
$ pip install gunicorn 
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/gunicorn.png)

# creation d'un fichier requirements.txt a la racine du projet avec la commande :

$ pip freeze > requirements.txt

supprimer  pkg-resources==0.0.0 si problemme signaler lors du push
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/requirements.png)

cela incluera tous packages les utiliser pour faire tourner l'app 
# creation dun fichier Procfile sans extention a la racine du projet
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/procfile.png)

# declarer debug a false dans settings.py
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/debug.png)

# rassembler les fichier static dans un dossier ecrire dans settings.py :
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/staticroot.png)


# collecter les fichier static avec la commande :
$ python manage.py collecstatic
![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/collectstatic.png)

# ajouter  commiter et pusher sur heroku

$ git add -A

$ git commit -m "add app in heroku"

$ heroku git:remote -a testederherokuapptuto

$ git push origin master

![alt text](https://raw.githubusercontent.com/Nicolas-Turck/Tuto-deployement-heroku/master/heroku_project/media/pushheroku.png)


 