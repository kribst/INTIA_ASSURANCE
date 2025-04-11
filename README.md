3. Installer Django
Installez Django dans votre environnement virtuel :

bash

Copier
pip install django
4. Créer un projet Django
Créez un nouveau projet Django :

bash

Copier
django-admin startproject nom_du_projet
cd nom_du_projet
5. Lancer le serveur de développement
Démarrez le serveur de développement pour tester votre application :

bash

Copier
python manage.py runserver
Accédez à http://127.0.0.1:8000 dans votre navigateur.

Déploiement sur PythonAnywhere
1. Créer un compte PythonAnywhere
Inscrivez-vous sur PythonAnywhere.

2. Créer un nouveau projet
Connectez-vous à PythonAnywhere.
Allez dans l'onglet "Web" et cliquez sur "Add a new web app".
3. Choisir le framework
Sélectionnez "Django" et choisissez la version de Python que vous utilisez.

4. Configurer le projet
Charger votre code :
Utilisez Git pour cloner votre dépôt ou téléchargez vos fichiers directement via l'interface de PythonAnywhere.
Exemple pour cloner :
bash

Copier
git clone https://github.com/username/repo.git
Installer les dépendances :
Accédez à votre console PythonAnywhere et installez les dépendances :
bash

Copier
pip install -r /path/to/your/requirements.txt
Configurer la base de données :
Si vous utilisez SQLite, vérifiez que le fichier de base de données est bien inclus.
Pour d'autres bases de données (comme MySQL), configurez-les dans votre projet.
5. Modifier les paramètres Django
Dans settings.py, modifiez les configurations suivantes :

ALLOWED_HOSTS :
python

Exécuter

Copier
ALLOWED_HOSTS = ['votre_nom_domaine.pythonanywhere.com']
Base de données :
Configurez la base de données si nécessaire.
6. Collecter les fichiers statiques
Exécutez la commande suivante pour collecter les fichiers statiques :

bash

Copier
python manage.py collectstatic
7. Configurer le fichier WSGI
Modifiez le fichier WSGI pour pointer vers votre application Django. Cela se trouve dans l'onglet "Web" sous "WSGI configuration file".

8. Redémarrer l'application
Après avoir configuré votre application, redémarrez-la depuis l'interface de PythonAnywhere.

9. Vérifier le déploiement
Accédez à votre application via l'URL fournie par PythonAnywhere pour vérifier que tout fonctionne correctement.
