# Choix de l'entreprise:

- Association de distributions de nourritures

# Critères de l'entreprise

Distribuer de la nourriture à des personnes dans le besoin.

1. Les personnes mariées sont priviligées par rapport au célibataires

2. Les personnes mariées avec des enfants sont priviligées par rapport aux personnes mariées sans enfants.

3. Les personnes handicapées sont les plus priviligées.

4. Definir une architecture de l'association

categories :

- Married :

  1. children : True
     ont aide les personnes mariées y compris leurs enfants
     - definir les produits necessaires pour un enfant
     - definir les produits suffisants pour les parents
  2. children : False
     ont aide les personnes mariées
     - definir les produits necessaires les mariées

- Single
  1. definir les produits necessaires la personne célibataire

Nous allons travailler avec deux bases de données distintes:

- Admin_db : pour les personnes de l'association

- Person_db : pour les personnes aidées par l'association

# I. database Person_db

Les differents entités sont les suivantes :

1. # Person

   - id : integer

   - firstname : string

   - lastname : string

   - gender : Enum("Male","Female")

   - email : string

   - phone : string

   - married : boolean

   - childcount : integer

   - age : interger

   - createdAt : Date

   - updatedAt : Date

   - deleteAt : Date

2. # Address

   - id : integer

   - country : Enum("France")

   - city : string

   - postalcode : string

   - sector : string

   - createdAt : Date

   - updatedAt : Date

3. # Documents

   - id : integer

   - path : string

   - createdAt : Date

   - updatedAt : Date

   - deleteAt : Date

4. # Products

   - id : integer

   - productname : string

   - createdAt : Date

   - updatedAt : Date

5. # Donation

   - id : integer

   - title : string

   - personId : integer

   - createdAt : Date

   - updatedAt : Date

# II. database Admin_db

1. user :

   - id :integer

   - firstname :string

   - lastname :string

   - AddressId

   - phone : string

   - fonction : string

   - createdAt : Date

   - updatedAt : Date

   - deleteAt : Date

2. # Address

   - id : integer

   - country : Enum("France")

   - city : string

   - postalcode : integer

   - sector : string

   - createdAt : Date

   - updatedAt : Date

3. # Activity

   - id : integer

   - title : string

   - projectId : int

   - createdAt : Date

   - updatedAt : Date

4. # project

   - id : integer

   - title : string

   - city : string

   - postalcode : integer

   - sector : string

   - createdAt : Date

   - updatedAt : Date

   - deleteAt : Date

