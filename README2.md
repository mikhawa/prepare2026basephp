# Manuel de Formation Intégral : Développement Web Backend 

## PHP Procédural et Algorithmique

### Introduction et Philosophie 

#### Pédagogique

Ce rapport constitue un manuel de formation exhaustif et rigoureux destiné aux formateurs et aux stagiaires débutant dans le développement web, avec une spécialisation sur le langage PHP dans une approche procédurale. Conformément aux exigences pédagogiques modernes et aux besoins spécifiques des centres de formation professionnelle, ce cursus est structuré pour assurer une progression linéaire : acquisition de la logique algorithmique fondamentale, maîtrise de la syntaxe PHP, manipulation avancée des structures de données, et interaction sécurisée avec les bases de données via PDO.Bien que l'écosystème PHP contemporain soit largement dominé par la Programmation Orientée Objet (POO) et les frameworks complexes (Symfony, Laravel), l'apprentissage initial du paradigme procédural demeure une étape pédagogique incontournable. Il permet aux apprenants de comprendre le flux d'exécution séquentiel, la gestion d'état et la logique brute sans la surcharge cognitive liée à l'abstraction des classes et des objets. L'unique exception à cette règle procédurale sera l'utilisation de l'extension PDO (PHP Data Objects) et la gestion des Exceptions, qui seront introduites comme des standards industriels indispensables pour garantir la sécurité et la portabilité des interactions avec les bases de données.Ce manuel alterne théorie approfondie, documentation technique référencée, et une densité maximale d'exercices pratiques ("Learning by Doing"), allant de l'algorithmique sur papier au développement d'applications web dynamiques complètes.Module 1 : Les Fondements de l'AlgorithmiqueAvant d'aborder la syntaxe spécifique du PHP, il est impératif de construire le socle logique de l'apprenant. L'algorithmique est l'art de décomposer un problème complexe en une suite finie et non ambiguë d'instructions élémentaires. C'est la "grammaire" universelle de la programmation, indépendante du langage utilisé.1.1 Concept de Variable et TypageEn algorithmique, une variable ne doit pas être vue simplement comme une lettre mathématique, mais comme une adresse mémoire nommée : une "boîte" étiquetée capable de contenir une information qui peut évoluer au cours du temps.Théorie de la Mémoire et des TypesLa gestion des types est cruciale. Contrairement à l'algèbre où $x$ peut être n'importe quoi, en informatique, la nature de la donnée définit les opérations possibles.Entier (Integer) : Représente les nombres sans virgule (..., -2, -1, 0, 1, 2...). Utilisé pour le dénombrement et les boucles.Réel (Float/Double) : Nombres à virgule flottante. Nécessaire pour les calculs de moyenne, prix, ou mesures physiques.Chaîne de caractères (String) : Suite de symboles alphanumériques. Même "123" est une chaîne s'il est entre guillemets.Booléen (Boolean) : Type logique binaire (VRAI ou FAUX). C'est le cœur des structures décisionnelles.Le cycle de vie d'une variable se décompose en deux phases :Déclaration : Allocation de l'espace mémoire (ex: Variable age : Entier).Affectation : Stockage d'une valeur (ex: age ← 25). Notez l'usage de la flèche ← pour distinguer l'affectation de l'égalité mathématique.Exercices d'Algorithmique : Variables et LogiqueExercice Algo 1.1 : L'échange des valeurs (Le problème du verre d'eau)Cet exercice est fondamental pour comprendre l'affectation séquentielle.Contexte : Soit deux variables A et B. A contient la valeur 5, B contient la valeur 12.Objectif : Écrire un algorithme permettant d'inverser les contenus. À la fin, A doit valoir 12 et B doit valoir 5.Contrainte : Vous ne pouvez pas faire A ← 12 directement (les valeurs sont inconnues au départ).Solution commentée :Il est impossible d'écrire A ← B puis B ← A, car la valeur initiale de A serait écrasée dès la première instruction. Il faut introduire une variable temporaire (le "troisième verre").DébutVariables A, B, Temp : EntiersA ← 5B ← 12Temp ← A    (On sauvegarde le contenu de A dans Temp. Temp vaut 5)A ← B       (On écrase A avec la valeur de B. A vaut 12)B ← Temp    (On récupère la valeur sauvegardée. B vaut 5)FinExercice Algo 1.2 : Calcul d'expressionsObjectif : Prédire la valeur finale des variables.DébutVariables X, Y, Z : EntiersX ← 2Y ← X + 3X ← 5Z ← X * YFinQuestion : Que valent X, Y et Z à la fin? (Réponse : X=5, Y=5, Z=25). Cela démontre que l'affectation Y ← X + 3 utilise la valeur de X au moment de l'instruction, sans lien dynamique futur.1.2 Structures Conditionnelles (Logique Booléenne)Un programme linéaire est limité. L'intelligence logicielle naît de la capacité à prendre des décisions via la structure SI... ALORS... SINON.Table de Vérité et OpérateursPour construire des conditions complexes, il faut maîtriser les opérateurs de comparaison et logiques.OpérateurSignificationExemple (Si A=10, B=5)Résultat==ÉgalitéA == BFAUX!=DifférenceA!= BVRAI>Supérieur strictA > 5VRAI>=Supérieur ou égalA >= 10VRAIET (AND)Conjonction(A > 5) ET (B < 2)FAUXOU (OR)Disjonction(A > 5) OU (B < 2)VRAIExercices d'Algorithmique : ConditionsExercice Algo 1.3 : Le Tarif CinémaÉnoncé : Un cinéma applique les tarifs suivants :Moins de 12 ans : 4 €De 12 à 18 ans (inclus) : 6 €Étudiant (quel que soit l'âge) : 5 €Adulte : 8 €Consigne : Écrire l'algorithme qui demande l'âge et le statut étudiant, puis affiche le prix à payer. Note : L'ordre des tests est crucial.Exercice Algo 1.4 : Le Maximum de trois nombresÉnoncé : Demander trois nombres à l'utilisateur. Sans utiliser de fonction prédéfinie, déterminer et afficher le plus grand des trois. Cet exercice entraîne à l'usage des SI imbriqués.1.3 Structures Itératives (Boucles)L'automatisation des tâches répétitives repose sur les boucles. Deux grandes familles existent.La Boucle "POUR" (Itérative) : Utilisée lorsque le nombre de répétitions est connu à l'avance.La Boucle "TANT QUE" (Conditionnelle) : Utilisée lorsque la répétition dépend d'une condition externe ou d'un événement (ex: saisie utilisateur).Exercices d'Algorithmique : BouclesExercice Algo 1.5 : La Somme CumulativeÉnoncé : Écrire un algorithme qui demande un nombre entier $N$ et calcule la somme de tous les entiers de 1 à $N$.Exemple : Si $N=5$, Résultat = $1+2+3+4+5 = 15$.Défi : Réaliser cet exercice avec une boucle POUR puis avec une boucle TANT QUE.Exercice Algo 1.6 : Contrôle de saisie strictÉnoncé : Demander à l'utilisateur un nombre compris entre 10 et 20.Si le nombre est < 10, afficher "Plus grand!".Si le nombre est > 20, afficher "Plus petit!".Répéter la demande tant que la saisie n'est pas valide.Ressources complémentaires Algo :Cours complet sur Developpez.com.Exercices de logique sur France-IOI.Module 2 : Syntaxe et Fondamentaux du Langage PHPUne fois la logique acquise, nous passons à son implémentation technique. PHP (Hypertext Preprocessor) est un langage de script exécuté côté serveur, conçu spécialement pour le développement web.2.1 Environnement et Fonctionnement Client-ServeurContrairement au HTML/CSS ou au JavaScript qui s'exécutent dans le navigateur du client, le PHP s'exécute sur le serveur web (Apache ou Nginx).Le client demande une page .php.Le serveur lance l'interpréteur PHP.PHP exécute les instructions (calculs, accès base de données).PHP génère un flux HTML pur qui est renvoyé au client. Le code source PHP est invisible pour l'utilisateur final.2.2 Balises et InstructionsTout code PHP doit être encapsulé dans les balises <?php et ?>. Si le fichier ne contient que du PHP, la balise fermante est omise pour éviter l'injection accidentelle d'espaces blancs.Chaque instruction se termine obligatoirement par un point-virgule ;.Les commentaires (invisibles à l'exécution) s'écrivent // (ligne) ou /*... */ (bloc).2.3 Variables et ConcaténationEn PHP, le typage est dynamique (le type est déduit de la valeur) et faible (les conversions sont automatiques). Toutes les variables sont préfixées par le sigle $.La ConcaténationPour assembler des chaînes de caractères, PHP utilise l'opérateur point ..PHP<?php
$prenom = "Jean";
$age = 25;

// Concaténation simple (guillemets simples)
echo 'Bonjour, je suis '. $prenom. ' et j\'ai '. $age. ' ans.';

// Interpolation (guillemets doubles)
// PHP interprète les variables à l'intérieur des guillemets doubles.
echo "Bonjour, je suis $prenom et j'ai $age ans.";
?>
Attention : Les guillemets simples ' sont plus performants car PHP ne cherche pas de variable à l'intérieur. Ils affichent le texte littéralement (sauf pour l'échappement \').2.4 Opérateurs Arithmétiques et MathématiquesPHP supporte les opérations classiques : +, -, *, /, et le modulo % (reste de la division entière).Exercices PHP : Premiers ScriptsExercice PHP 2.1 : Traduction "Hello World"Consigne : Créer un fichier index.php. Définir une variable $nom. Afficher "Bonjour [nom], bienvenue dans le cours PHP!" dans une balise HTML <h1>.Exercice PHP 2.2 : Calculatrice TVAConsigne :Définir une variable $prixHT (ex: 50).Définir une variable $tauxTVA (ex: 1.21 pour 21%).Calculer le $prixTTC et l'afficher avec une phrase explicative.Utiliser la fonction number_format() pour limiter l'affichage à 2 décimales.Exercice PHP 2.3 : L'échange de variables (Implémentation)Consigne : Reprendre l'algorithme 1.1 et le coder en PHP. Utiliser echo pour afficher les états avant et après l'échange.Module 3 : Structures de Contrôle PHPLa syntaxe PHP pour les conditions et les boucles est héritée du langage C, ce qui la rend très standard.3.1 Les Conditions (If, Else, Switch)Structure IF... ELSEC'est la traduction directe de l'algorithme SI...SINON.PHP<?php
$note = 12;

if ($note >= 16) {
    echo "Très bien";
} elseif ($note >= 12) { // Sinon Si
    echo "Bien";
} elseif ($note >= 10) {
    echo "Moyen";
} else {
    echo "Insuffisant";
}
?>
Point de vigilance : Ne confondez pas l'opérateur d'affectation = avec l'opérateur de comparaison == (égalité de valeur) ou === (égalité de valeur ET de type). 0 == "0" est VRAI, mais 0 === "0" est FAUX.Structure SWITCHIdéale pour tester une même variable contre plusieurs valeurs constantes.PHPswitch ($codePays) {
    case 'FR':
        echo "France";
        break; // Indispensable pour ne pas exécuter le cas suivant
    case 'BE':
        echo "Belgique";
        break;
    default:
        echo "Pays inconnu";
}
Exercices PHP : Logique ConditionnelleExercice PHP 3.1 : Le calculateur d'IMC avancéConsigne :Définir variables $poids (kg) et $taille (m).Calculer l'IMC = $poids / taille^2$.Selon le résultat, afficher l'interprétation (ex: < 18.5 : Maigreur, 18.5-25 : Normal, > 25 : Surpoids).Exercice PHP 3.2 : Date et HeureConsigne : Utiliser la fonction native date('H') pour récupérer l'heure actuelle du serveur.Si l'heure est entre 05h et 12h : Afficher "Bon matin".Entre 12h et 18h : "Bon après-midi".Sinon : "Bonne soirée".3.2 Les Boucles (While, For, Do-While)La boucle WHILE (Tant que)Vérifie la condition avant d'exécuter le bloc. Si la condition est fausse dès le départ, le code n'est jamais exécuté.PHP$i = 0;
while ($i < 10) {
    echo $i. " ";
    $i++; // Incrémentation
}
La boucle FOR (Pour)Rassemble l'initialisation, la condition et l'incrémentation sur une seule ligne. C'est la boucle préférée pour les compteurs.PHPfor ($i = 0; $i < 10; $i++) {
    echo "Tour n°$i <br>";
}
Exercices PHP : ItérationsExercice PHP 3.3 : Les tables de multiplication (HTML)Consigne : Écrire un script qui génère la table de multiplication de 8. Le résultat doit être affiché dans un tableau HTML <table>.Astuce : La balise <table> doit être ouverte avant la boucle et fermée après. Les <tr> et <td> sont générés à l'intérieur de la boucle.Exercice PHP 3.4 : Punition dynamiqueConsigne : Créer une boucle qui affiche 100 fois une phrase, mais où le numéro de la ligne apparaît en gras (ex: 1 Je ne dois pas... 2 Je ne dois pas...).Module 4 : Structures de Données Complexes – Les TableauxEn PHP, les tableaux (Arrays) sont des structures extrêmement puissantes et flexibles. Ils peuvent se comporter comme des listes, des dictionnaires, des piles ou des files.4.1 Tableaux Indexés (Numérotés)Les clés sont des indices numériques générés automatiquement, commençant toujours à 0.PHP// Déclaration (Syntaxe courte, recommandée depuis PHP 5.4)
$fruits =; 

// Accès
echo $fruits; // Affiche "Pomme"

// Ajout
$fruits = "Orange"; // Ajoute à la fin (indice 3)

// Debug
print_r($fruits); // Affiche la structure brute pour le développeur
4.2 Tableaux AssociatifsLes clés sont des chaînes de caractères définies par le développeur. C'est essentiel pour structurer des données sémantiques.PHP$stagiaire =;

echo $stagiaire["prenom"]; // Affiche Marie
4.3 Tableaux MultidimensionnelsUn tableau peut contenir d'autres tableaux. C'est la structure standard pour gérer des listes d'enregistrements (ex: liste de produits, liste d'utilisateurs).PHP$classe = ["nom" => "A", "note" => 15],
   ,
    ["nom" => "C", "note" => 18];

echo $classe["note"]; // Affiche 18
4.4 La Boucle FOREACHC'est la structure de contrôle dédiée au parcours de tableaux. Elle est plus lisible et plus sûre que la boucle for pour les tableaux.PHPforeach ($stagiaire as $cle => $valeur) {
    echo ucfirst($cle). " : ". $valeur. "<br>";
}
Exercices PHP : Manipulation de TableauxExercice PHP 4.1 : Moyenne et ExtrêmesConsigne : Créer un tableau indexé contenant 10 notes aléatoires (entre 0 et 20).Parcourir le tableau pour calculer la moyenne de la classe.Déterminer la note minimale et maximale (sans utiliser min() ou max() dans un premier temps pour travailler l'algorithmique).Afficher le tout proprement.Exercice PHP 4.2 : Le catalogue produitsConsigne : Créer un tableau multidimensionnel représentant 3 produits (Nom, Prix, Stock).Afficher ces produits dans un tableau HTML.Si le stock est < 3, afficher le chiffre en rouge (gestion de condition dans la boucle).Calculer la valeur totale du stock (Prix * Quantité pour chaque produit).Exercice PHP 4.3 : DépartementsConsigne : Créer un tableau associatif [CodePostal => NomVille].Afficher une liste déroulante HTML (<select>) générée dynamiquement à partir de ce tableau. La clé doit être la value de l'option, et le nom de la ville le texte affiché.Module 5 : Fonctions et Organisation du CodeL'approche procédurale repose sur la découpe du problème en sous-problèmes résolus par des fonctions. Cela évite la répétition de code (principe DRY : Don't Repeat Yourself) et améliore la maintenance.5.1 Déclaration et AppelUne fonction est un bloc de code nommé qui peut recevoir des paramètres et retourner une valeur.PHP/**
 * Calcule le prix TTC
 * @param float $prixHT Prix hors taxes
 * @param float $taux Taux de conversion (ex: 1.21)
 * @return float Prix TTC
 */
function calculerTTC($prixHT, $taux = 1.21) { // Paramètre par défaut
    $resultat = $prixHT * $taux;
    return $resultat;
}

$produitA = calculerTTC(100);       // Utilise le taux par défaut (1.21) -> 121
$produitB = calculerTTC(100, 1.06); // Surcharge le taux -> 106
Portée (Scope) : Les variables définies à l'intérieur d'une fonction sont locales. Elles n'existent pas à l'extérieur. Les variables extérieures ne sont pas visibles dedans (sauf passage en paramètre).5.2 Inclusions de FichiersPour structurer un projet, on sépare le code en fichiers logiques.include / include_once : Génère un avertissement si le fichier manque (le script continue).require / require_once : Génère une erreur fatale si le fichier manque (le script s'arrête). À privilégier pour les fichiers critiques (config, fonctions).Exercices PHP : ModularitéExercice PHP 5.1 : Bibliothèque MathématiqueConsigne :Créer un fichier maths.php. Y définir des fonctions : add($a,$b), sub($a,$b), multiply($a,$b), divide($a,$b) (avec gestion de la division par zéro).Créer index.php. Inclure maths.php. Utiliser ces fonctions pour effectuer des calculs et afficher les résultats.Exercice PHP 5.2 : Générateur de HTMLConsigne : Créer une fonction genererTableau($data) qui prend un tableau PHP en paramètre et retourne une chaîne de caractères contenant le code HTML d'un <table> complet représentant ces données. Tester avec le tableau de l'exercice 4.2.Module 6 : Interaction Web – Formulaires et SuperglobalesC'est l'étape où le script PHP devient interactif et traite les données envoyées par l'utilisateur.6.1 Les SuperglobalesPHP met à disposition des variables tableaux accessibles partout (d'où le nom "Superglobales").$_GET : Contient les paramètres passés dans l'URL. Visible, limité en taille, utilisé pour la navigation.$_POST : Contient les données envoyées par le corps de la requête HTTP. Invisible dans l'URL, utilisé pour les formulaires sensibles (mots de passe, données longues).$_SERVER : Informations techniques (IP du client, méthode de requête, chemin du script).6.2 Traitement des FormulairesLe traitement se fait généralement en deux temps : vérification de l'envoi, puis validation des données.PHP// Vérifier si le formulaire a été soumis
if ($_SERVER == "POST") {
    
    // Vérifier l'existence et que ce n'est pas vide
    if (isset($_POST['email']) &&!empty($_POST['email'])) {
        
        // Nettoyage et Sécurité (Sanitization)
        $email = htmlspecialchars($_POST['email']);
        
        echo "Email reçu : ". $email;
    } else {
        echo "L'email est obligatoire.";
    }
}
Sécurité XSS (Cross-Site Scripting) : Un attaquant peut tenter d'envoyer du code JavaScript (<script>alert('hack')</script>) dans un champ. L'affichage direct de cette variable exécuterait le code. La fonction htmlspecialchars() convertit les caractères spéciaux en entités HTML inoffensives.Exercices PHP : FormulairesExercice PHP 6.1 : Le DevinConsigne :Le script choisit un nombre aléatoire (stocké, ou fixe pour simplifier au début).L'utilisateur propose un nombre via un formulaire.Le script compare et affiche "Trop grand", "Trop petit" ou "Gagné".Exercice PHP 6.2 : Convertisseur de DevisesConsigne : Créer un formulaire avec :Un champ montant.Une liste déroulante (EUR vers USD, USD vers EUR).Au clic sur "Convertir", afficher le résultat en utilisant un taux fixe (ex: 1.10).Le formulaire doit "retenir" la valeur saisie (Sticky form).Module 7 : Persistance des Données – Base de Données et PDOPour qu'une application soit utile, elle doit stocker les données durablement. Nous utiliserons MySQL (ou MariaDB) et l'interface d'abstraction PDO (PHP Data Objects).7.1 Pourquoi PDO?PDO est la méthode standard et sécurisée pour accéder aux bases de données en PHP. Contrairement aux anciennes fonctions mysql_ (obsolètes) ou mysqli_ (spécifique MySQL), PDO permet de changer de système de base de données (passer à PostgreSQL ou SQLite) sans réécrire tout le code. Elle supporte nativement les Exceptions et les Requêtes Préparées.7.2 Connexion et Gestion des Erreurs (Exceptions)La connexion est une opération risquée (serveur éteint, mot de passe faux). Nous devons utiliser un bloc try... catch pour attraper ("catch") l'erreur ("Exception") si elle survient, afin d'éviter d'afficher des mots de passe à l'écran.PHP$dsn = "mysql:host=localhost;dbname=formation_php;charset=utf8";
$user = "root";
$pass = ""; // À adapter selon configuration (ex: 'root' sur MAMP)

try {
    // Tentative de connexion
    $pdo = new PDO($dsn, $user, $pass);
    
    // Configuration pour lever des exceptions en cas d'erreur SQL
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    // Configuration pour le mode de récupération par défaut (Tableau associatif)
    $pdo->setAttribute(PDO::ATTR_DEFAULT_FETCH_MODE, PDO::FETCH_ASSOC);
    
} catch (PDOException $e) {
    // En cas d'erreur, on arrête tout proprement
    die("Erreur de connexion BDD : ". $e->getMessage());
}
7.3 Lecture de Données (SELECT)Pour lire des données, on utilise query() si la requête n'a pas de paramètres, ou prepare() sinon.PHP$sql = "SELECT * FROM utilisateurs";
$stmt = $pdo->query($sql); // stmt = statement (état)

// Récupérer tout d'un coup
$users = $stmt->fetchAll();

foreach ($users as $u) {
    echo $u['nom']. "<br>";
}
7.4 Écriture Sécurisée (Requêtes Préparées)C'est le point de sécurité le plus critique du cours. L'injection SQL survient quand on concatène une variable utilisateur directement dans le SQL.Mauvais : "SELECT * FROM users WHERE id = ". $_POST['id'] (Danger!)Bon : Utiliser des marqueurs nommés (:id) ou positionnels (?).PHP// Préparation de la requête (le SGBD analyse la structure, pas les données)
$sql = "INSERT INTO utilisateurs (nom, email, age) VALUES (:nom, :email, :age)";
$stmt = $pdo->prepare($sql);

// Exécution en liant les valeurs
$succes = $stmt->execute();

if ($succes) {
    echo "Utilisateur ajouté!";
}
Exercices PHP : Base de DonnéesExercice PHP 7.1 : Liste des StagiairesConsigne :Créer une table stagiaires (id, nom, prenom, date_naissance) dans PHPMyAdmin.Insérer manuellement 3 stagiaires.Créer une page PHP qui se connecte et affiche la liste dans un tableau HTML propre.Exercice PHP 7.2 : Formulaire d'inscriptionConsigne :Créer un formulaire HTML (Nom, Prénom).En PHP, traiter le formulaire et insérer les données dans la table via une requête préparée.Afficher un message de confirmation.Module 8 : Gestion d'État – Sessions et CookiesLe protocole HTTP est "stateless" (sans état). Le serveur oublie qui vous êtes dès que la page est envoyée. Les sessions permettent de "garder le fil".8.1 Mécanisme des SessionsUne session crée un fichier temporaire sur le serveur et stocke un identifiant unique (Session ID) dans un cookie sur le navigateur du client.Démarrage : session_start() doit être la toute première instruction du fichier (avant tout HTML ou echo).Stockage : On utilise la superglobale $_SESSION.Destruction : session_destroy() (pour la déconnexion).PHP// page1.php
session_start();
$_SESSION['pseudo'] = "Administrateur";

// page2.php
session_start();
if (isset($_SESSION['pseudo'])) {
    echo "Bonjour ". $_SESSION['pseudo'];
} else {
    echo "Vous n'êtes pas connecté.";
}
Exercices PHP : SessionsExercice PHP 8.1 : Authentification simpleConsigne :Créer un formulaire de login (login/password).Si login="admin" et pass="12345", démarrer une session et stocker le statut connecté.Rediriger vers une page dashboard.php (utiliser header('Location: dashboard.php');).Sur dashboard.php, vérifier si la session est active. Sinon, rediriger vers le login (Sécurisation de page).Projet Fil Rouge : Le Livre d'OrPour valider l'ensemble des acquis, les stagiaires réaliseront un "Livre d'Or". Ce projet synthétise : Formulaires, PDO, Sécurité (XSS/SQL), et Algorithmique (tri/affichage).Cahier des ChargesBase de données : Créer une table messages avec les colonnes id, auteur, contenu, date_creation.Interface : Une page unique livreor.php.Fonctionnalités :Un formulaire en haut de page pour laisser un message.Affichage en dessous de tous les messages précédents, du plus récent au plus ancien.Les dates doivent être formatées en français (ex: "le 14/02/2026 à 14h30").Contraintes Techniques :Utilisation de PDO avec exceptions.Requêtes préparées obligatoires pour l'insertion.Protection htmlspecialchars obligatoire à l'affichage.Validation : Le message ne doit pas être vide.Algorithme du ProjetConnexion BDD.Si le formulaire est posté :Vérifier les champs.Préparer l'INSERT.Exécuter l'INSERT.(Optionnel) Rediriger vers la même page pour éviter le renvoi du formulaire au rafraîchissement (Pattern PRG : Post-Redirect-Get).Exécuter un SELECT (ORDER BY date_creation DESC).Boucler (foreach) sur les résultats pour générer le HTML.Ressources et AnnexesPour soutenir l'apprentissage continu, voici une sélection de ressources validées :Documentation de RéférenceRessourceDescriptionLienManuel PHPLa documentation officielle, très complète et traduite.php.net/manual/frPHP PDORéférence spécifique pour l'extension de base de données.php.net/manual/fr/book.pdo.phpDeveloppez.comCours d'algorithmique très détaillés.algo.developpez.comLearn-PHPTutoriels interactifs pour tester le code en direct.learn-php.org/frOutils RecommandésÉditeur de code : Visual Studio Code (avec extensions PHP Intelephense).Serveur local : XAMPP (Windows), MAMP (Mac), ou Laragon (Windows - recommandé pour sa simplicité).Débogage : Apprendre à utiliser var_dump() et die() est essentiel au début, avant de passer à Xdebug.Ce manuel couvre l'intégralité du socle technique nécessaire pour un développeur backend junior. La maîtrise de ces concepts procéduraux est le prérequis indispensable avant d'aborder la Programmation Orientée Objet et les frameworks MVC modernes.