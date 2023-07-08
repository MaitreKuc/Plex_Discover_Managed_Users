# Plex_Discover_Managed_Users
Plex Discover for managed users

En français / in french :

De base, la fonction "Découvrir" n'est pas disponible pour les utilisateurs gérés, et la plupart des personnes utilisent leur compte admin seulement pour les réglages et la maintenance.
Donc j'ai regardé un peu le code source de la page web au niveau de ce paramètre et je vois que les valeurs pour "Découvrez" et "Plus de façon de regarder" ont seulement "opt_out" et "opt_out_managed".
Mais sur l'option en dessous, je vois une valeur en plus, "opt_in".
Je modifie donc la valeur de l'option "Découvrez" sans grande conviction que ça fonctionne, et là ça fonctionne quand même.

Donc voici les étapes à suivre :
- Connectez-vous à votre serveur plex via un navigateur.
- Allez dans les paramètres de compte avec le compte admin
- Puis "Service en ligne" (en haut à gauche)
- Allez à la section "Découvrir"
- Cliquez sur modifier.
- Allez sur la liste déroulante et faites clic droit, puis inspecter
- Normalement, vous devriez être au niveau du select avec l'ID : InconnexingDiscoverSource
- Cliquez sur la flèche à côté du "select", vous devriez voir apparaître '<option value="opt_out_managed"...>' et '<option value="opt_out"...>'
- ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/38bf5552-ff4e-45e6-8f14-864a48f4d246)
- Cliquez sur 'opt_out' ou "opt_out_managed" et changez la valeur par 'opt_in'
- ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/0592eaf1-359a-46cf-a899-058cb9181c05)
- Si vous avez changé la valeur de 'opt_out', alors sélectionnez "Désactiver" dans la liste déroulante. Et si vous avez changé la valeur de "opt_out_managed", sélectionnez "Désactiver pour les utilisateurs gérés"
- Puis cliquez sur "Enregistrer les modifications"
- Et voilà, l'option sera disponible pour vos comptes gérés.

Pour vérifier si la manipulation à fonctionner, retournez sur la liste déroulante et normalement la valeur sélectionnée sera "opt_in".
Aussi, connectez-vous avec un compte géré et dans la barre latérale à gauche, vous devriez avoir "Découvrez", s'il n'est pas présent, sélectionnez le "Plus" et épingler "Découvrez".

![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/fba0f608-d941-4acc-8d81-de7fdd4de2ee) ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/972d0597-4c90-4988-937b-701a430e3e4c)



A savoir:

Grâce à cette astuce, ![Plex_Debrid](https://github.com/itsToggle/plex_debrid) fonctionne avec tout les utilisateurs. Il suffit juste d'ajouter les utilisateurs dans Plex_Debrid avec leur bon Token.
Quand vous êtes connecté sur un compte d'utilisateur géré, faites un clic droit puis "Inspecter", puis aller dans l'onglet "Réseau", sélectionnez une requête (si vide, cliquez sur un média) et cherchez la valeur de "X-Plex-Token".
![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/eb76e6f1-9b97-4d3b-9cca-a7b1ce72ce14)



En anglais / in english :

Basically, the "Discover" function is not available for managed users, and most people use their admin account only for settings and maintenance.
So I looked a bit at the source code of the web page at this parameter and I see that the values ​​for "Discover" and "More way to watch" have only "opt_out" and "opt_out_managed".
But on the option below, I see an extra value, "opt_in".
So I modify the value of the "Discover" option without much conviction that it works, and there it works anyway.

So here are the steps to follow:
- Connect to your plex server through a browser.
- Go to account settings with admin account
- Then "Online service" (top left)
- Go to the "Discover" section
- Click modify.
- Go to the dropdown and right click, then inspect
- Normally, you should be at the select level with ID: InconnexingDiscoverSource
- Click on the arrow next to the "select", you should see '<option value="opt_out_managed"...>' and '<option value="opt_out"...>'
- ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/38bf5552-ff4e-45e6-8f14-864a48f4d246)
- Click on 'opt_out' or 'opt_out_managed' and change the value to 'opt_in'
- ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/0592eaf1-359a-46cf-a899-058cb9181c05)
- If you changed the value of 'opt_out', then select 'Disable' from the drop-down list. And if you changed the value of "opt_out_managed", select "Disable for managed users"
- Then click "Save Changes"
- And that's it, the option will be available for your managed accounts.

To check if the manipulation worked, return to the drop-down list and normally the selected value will be "opt_in".
Also, sign in with a managed account and in the sidebar on the left you should have "Discover", if it's not present, select the "More" and pin "Discover".

![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/fba0f608-d941-4acc-8d81-de7fdd4de2ee) ![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/972d0597-4c90-4988-937b-701a430e3e4c)

To know:

Thanks to this trick, ![Plex_Debrid](https://github.com/itsToggle/plex_debrid) works with all users. Just add users in Plex_Debrid with their correct Token.
When you are connected to a managed user account, right click then "Inspect", then go to the "Network" tab, select a query (if empty, click on a media) and look for the value of "X -Plex-Token".
![image](https://github.com/MaitreKuc/Plex_Discover_Managed_Users/assets/30301747/eb76e6f1-9b97-4d3b-9cca-a7b1ce72ce14)
