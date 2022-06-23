Knygų rezervacijos aplikacija PHP programuotojo kvalifikacijos egzaminui.

Aplikacija kurta naudojant LARAVEL, kuris yra PHP programavimo kalbos karkasas. Vartotojo sąsajai kurti naudotas REACT, JavaScript kalbos karkasas. Duomenų bazei naudojamas MySQL.

***

Duomenų bazės struktūra:
Lentelės:
    - Knygos:
            - ISBN: INTEGER (primary key)
            - Pavadinimas: VARCHAR(255)
            - Aprašymas: TEXT
            - Kategorija: VARCHAR(255) (foreign key --> Kategorijos)
            - Nuoroda į paveikslėlį: VARCHAR(255)
            - Puslapių skaičius: INTEGER(4)
            - Kiekis: INTEGER(2)
    - Kategorijos:
            - ID: INTEGER (primary key)
            - Kategorijos pavadinimas: VARCHAR(255)
    - Vartotojai:
            - ID: INTEGER (primary key)
            - El. paštas: VARCHAR(255)
            - Slaptažodis: VARCHAR(255)
    - Rolės:
            - ID: INTEGER (primary key)
            - Rolės pavadinimas: VARCHAR(255)
    - Vartotojų rolės:
            - Vartotojo ID: INTEGER (foreign key --> Vartotojai)
            - Rolės ID: INTEGER (foreign key --> Rolės)
    - Statusas:
            - ID: INTEGER (primary key)
            - Statuso pavadinimas: VARCHAR(255)
    - Rezervacijos:
            - ID: INTEGER (primary key)
            - Vartotojo ID: INTEGER (foreign key --> Vartotojai)
            - Knygos ISBN: INTEGER (foreign key --> Knygos)

***
Kaip pasileisti?

- klonuokite aplikaciją iš GitHub repositorijos naudodami GitHub Desktop programą;
- susikurkite lokalią repositoriją savo įrenginyje;
- GitHub Desktop pasirinkite "Atidaryti aplikaciją su Visual Studio Code";
- komandinėje eilutėje pasileiskite komandą "npm run watch";
- komandinėje eilutėje pasileiskite komandą "php artisan serve";
- sveikinu, jūs pasileidote knygų rezervacijos aplikaciją!
