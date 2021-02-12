---
title: API Service National
tagline: Vérifiez si un candidat est en règle vis-à-vis de ses obligations de Service National et peut s’inscrire au concours ou à l’examen dont vous êtes en charge.
access_page:
  - who:
      - Un particulier
      - Une entreprise
    is_eligible: -1
    description: |
      Vous ne pouvez pas accèder a ces informations.

      <Button href="/rechercher-api">Rechercher une autre API</Button>
  - who:
      - Un service chargé de l'inscription à un examen ou un concours soumis au controle de l'autorité publique
    is_eligible: 1
    description: |
      Conformément aux dispositions de <External href="https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000021960309/">Article L114-6</External> du *code du service national*, les personnes de moins de 25 ans assujettie à l'obligation de participer à la journée défense et citoyenneté doivent être en règle pour être autorisé à s'inscrire aux examens et concours soumis au contrôle de l'autorité publique.

      Dans le cadre de cette vérification, vous pouvez faire une demande d'accès à l'API :

      <NextSteps />
      <Button href="https://datapass-staging.api.gouv.fr/api-dsnj?demarche=inscription-examens">Remplir une demande</Button>
is_open: -1
producer: ministere-armees
keywords:
  - service
  - défense
  - journée
  - appel
  - National
  - armée
  - examens
themes:
  - Particulier
contact_link: dsn.contact-demarche.fct@intradef.gouv.fr
doc_tech_link: https://presaje.sga.defense.gouv.fr/api/doc
last_update: 01/02/2020
---

L'API Service National facilite la constitution des dossiers d'inscription aux examens et concours soumis au contrôle de l'autorité publique.

### À quoi sert l’API Service National ?

Elle permet aux administrations d'accéder à des informations certifiées à la source et ainsi :

- de s’affranchir des pièces justificatives lors des démarches en ligne ou physiques
- de réduire le nombre d’erreurs de saisie
- d'écarter le risque de fraude documentaire

Du point de vue de l’usager, une démarche qui utilise l’API Service national s'apparente à ça :

1. Je me connecte sur un site ou je me déplace en vue d'une inscription à un examen ou un concours.
2. Le service chargé de la constitution de mon dossier récupère ma situation au regard des obligations de service national. Si je suis en règle, je n’ai plus rien à faire !

### Données

L'API retourne selon le cas :

| Type de réponse | Description                                                                                                                                                                                                                 |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OK ou KO        | l'individu est connu, ou n'est pas connu de la base de données                                                                                                                                                              |
| En règle        | l'individu est en règle au regard des obligations de Service National                                                                                                                                                       |
| Pas en règle    | l'individu n'est pas en règle au regard des obligations de Service National                                                                                                                                                 |
| Indéterminée    | la situation de l'individu est complexe et nécessite un traitement par un agent. L'individu doit fournir les pièces justificatives en sa possession, ou à défaut contacter son centre du Service National et de la jeunesse |
| Non concerné    | l'individu n'est plus soumis à l'obligation de justifier de sa situation au regard des obligations de Service National                                                                                                      |

### Qui produit cette API ?

Au sein du ministère des Armées, c'est la Direction du Service National et de la Jeunesse (DSNJ) qui opère cette API.

### Qu’est ce que le Service National ?

Le service national universel comprend les obligations suivantes : le recensement, la journée défense et citoyenneté (et l'appel sous les drapeaux, suspendu).

Tout jeune Français doit se faire recenser dès l’âge de 16 ans, ce qui lui permet notamment d’être convoqué à la journée défense et citoyenneté (JDC) avant l’âge de 18 ans.

Le document remis à chacune de ces étapes permet de justifier d’une situation régulière, et ainsi de s’inscrire aux examens et concours soumis au contrôle de l’autorité publique.