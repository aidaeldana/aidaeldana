#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <time.h>

// Définition de la taile maximale de chaine de caractères pour les noms des athlètes//
#define MAXCHAR 100
#define MAXATH 300 
#define MAX_PARTICIPANTS_RELAIS 4 
 // Nombre maximal de participants au relais//

// Définition de l'énumeration pour représenter les différents épreuves//
typedef enum {
  _100m,
  _400m,
  _5000m,
  _marathon,
  _relais_4x400m,
} Epreuve;

// Défintion de la structure temps//
typedef struct {
  int minutes;
  double secondes;
} Temps;

typedef struct {
  char nom[MAXCHAR];
  char prenom[MAXCHAR];
  Epreuve epreuve;
  //char sexe; //'M' pour masculin, 'F' pour feminin//
  Temps *temps; // Pointeur vers un tableau dynamique pour stocker les temps de chaque épreuve//
} Athlete;    

// Structure pour représenter un participant au relais//
typedef struct {
  char nom[MAXCHAR];
  char prenom[MAXCHAR];
  //char sexe;
  int position; // position dans le relais (1ère, 2ème, 3ème ou 4ème)//
} ParticipantRelais;

// Structure pour représenter un entraînement//
typedef struct {
  char date[15]; // format de date : "JJ/MM/AAAA"
  Epreuve type_epreuve;
  Temps *temps;
  ParticipantRelais participants[MAX_PARTICIPANTS_RELAIS];
} Entrainement;

// Fonction pour créer le fichier de l'athlete//
void creer_fichier_athlete(char nomAthlete[]) {
  FILE *fichier = fopen("nomAthlete", "w"); // ouvrir le fichier en mode écriture//
  if (fichier == NULL) {
    printf("Ouverture du fichier %s impossible \n", nomAthlete);
    exit(1);
  }
  fclose(fichier);
}
//void ajout_perf(char nomAthlete[], Epreuve epreuve, Temps temps){}

// Fonction pour enregistrer les performances dans le fichier de l'athlete//
void enregistrer_entrainement_fichier(char nomAthlete[],Entrainement *entrainement){
FILE *fichier = fopen(nomAthlete, "a"); // ouvrir le fichier en mode ajout//
if (fichier == NULL) {
  printf("Erreur lors de la création du fichier %s\n", nomAthlete);
  exit(1);
}
  fprintf("fichier,"%s.%dmin%2lf \n",entrainement->date, entrainement->temps->minutes,entrainement->temps->secondes);
fclose(fichier);
}

// Fonction pour ajouter un nouvel athelete//
void ajouter_Athlete(Athlete *athlete, int *nb_athletes){
  printf("Entrez le nom de l'athlete ; ");
  scanf("%s", athlete[*nb_athletes].nom);
  printf("Entrez le prénom de l'athlète : ");
  scanf("%s",athlete[*nb_athletes].prenom);
  (*nb_athletes)++;
  printf("Le nouvel athlete est ajoute avec succès.\n");
}

//Fonction poour allouer la mémoire pour un tableau dynamique de temps//
//Temps *allouer_temps(int nb_epreuves){
  //Athlete->nb_epreuves=nb_epreuves;
  //thlete.temps = malloc(nb_epreuves* sizeof(Temps)); // Allocation dynmaique pour le tableau de temps//
  //if (athlete.temps == NULL) {
     //printf("Erreur d'allocation de mémoire\n");
     //exit(EXIT_FAILURE);
  //}
//}

    // Fonction pour ajouter un nouvel athlète//
    void ajouter_Athlète(Athlete *athlete, char nom[MAXCHAR],
                         char prenom[MAXCHAR], char sexe) {
  strcpy(athlete->nom, nom);
  strcpy(athlete->prenom, prenom);
  //athlete->sexe = sexe;
    }
 
 //Fonction pour supprimer un athlète - amélioration
 void supprimer_Athlete(Athlete *athlete, int *nb_athletes, char nom[MAXCHAR]){

  for(int j=i; *nb_athletes,j++){
    strcpy(athlete[]);
  }
 }     
      
  // Fonction pour enregistrer le temps d'un athlète pour une épreuve donnée//
  void enregistrer_temps(Athlete * athlete, Epreuve epreuve, Temps temps) {
    
  }

  // Fonction pour consulter le temps d'un athlète pour une épreuve//
  void consulter_temps(Athlete * athlete, Epreuve epreuve) {
    
  }

  // Fonction pour entrer les détails d'un nouvel entraînement
  void entrer_details() {
    
  }

  // Fontion pour permettre à l'entraîneur de consulter les statistiques de performances de chaque athlète - les meilleurs, pire temps et la moyenne pour chaque épreuve//
  void consulter_statistiques(){}

      // Fonction pour le résumé des performances d'un athlète//
  void resume_performances(nomAthlete, Epreuve epreuve, char date) {}
  // Fonction pour calculer les différences et comparer//
  // Fonction pour calculer la différence de temps entre les deux
  // entraînements//
void time_difference(Athlete *athlete, Epreuve epreuve, Temps t1, Temps t2, Temps *diff(){
  
}

//Fonction pour calculer l'équation de la droite d'évoltion des performances d'un athlète//


//Programme principal//
int main(){
      Athlete athlete;
  //le nombre maximal d'athletes//  int max_athletes=260;
  Athlete *athlete = malloc(max_athletes* sizeof(Athlete));
  int nb_athletes = 0;
  //Ajouter nouveaux athlètes
  ajouter_Athlete(athletes, &nb_athletes);
  // Liberez la mémoire allouée dynamiquement//
  free(athletes);
  
  // consultation des temps pour differents épreuves//
    printf("Temps pour le 100m est %2f");

  //Ajouter un nouvel athlete
//  Athlete athlete;
  printf("Entrez le nom de l'athlète : ");
  scanf("%s", athlete.nom);
  prinf("Entrez le prénom de l'athlète : ");
  scanf("%s", athlete.prenom);
  printf("Entrez le sexe de l'athlète (M ou F) : ");
  scanf("%c", &athlete.sexe);

  //d Demander à l'utilisateur de saisir lesdétailldes athletes
//  Entrainement entrainement;
  printf("Entrez la date de l'entraînement (format JJ/MM/AAAA) : ");
  scanf("%s", entrainement->date);
  printf("Entrez le type d'épreuve (100m, 400m, 5000m, marathon, relais 4x100m) : ");
  scanf("%s", entrainement->type_epreuve);
  printf("Entrez le temps de l'épreuve (format MM:SS) : ");
  scanf(" %d:%lf", &ntrainement, &temps->minutes, &entrainement->temps.secondes);
  
  //Enregistrer les perfomances dans le fichier
//  enregistrer_entrainement_fichier(nomAthlete,&entrainement);

  
  

        return 0;

<!---
aidaeldana/aidaeldana is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
