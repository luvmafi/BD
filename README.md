# Schema Bazei de Date pentru o Companie

Acest proiect prezintă schema unei baze de date SQL proiectată pentru a gestiona structura organizațională a unei companii, incluzând angajații, departamentele, echipele, proiectele, directorii, contractele și lansările de proiecte.

## Prezentare Generală

Baza de date include mai multe tabele, fiecare având un scop unic în ecosistemul companiei:

- `Angajat`: Conține detalii despre fiecare angajat, cum ar fi ID-ul, numele, salariul și data angajării.
- `Departament`: Listează toate departamentele din companie, fiecare departament având un ID unic și un nume.
- `Echipa`: Definește echipele din cadrul departamentelor, inclusiv ID-ul echipei, ID-ul departamentului, numele echipei și numărul de sarcini alocate.
- `Proiect`: Detalii despre proiecte, inclusiv ID-ul proiectului, numele, stadiul de completare și data prezentării.
- `Director`: Informații despre directorii companiei, inclusiv ID-ul, numele, salariul și data la care și-au asumat rolul.
- `Contract`: Contractele între companie și directorii săi, detaliind ID-ul contractului, ID-ul proiectului, ID-ul directorului, câștigurile contractului și data contractului.
- `Relase` (Lansare): Înregistrează asocierea între echipe și proiectele la care lucrează.

## Caracteristici Principale

- **Secvență pentru ID-uri Angajați**: O secvență (`secv_angajat`) este utilizată pentru a genera automat ID-uri unice pentru angajații noi.
- **Constrângeri Cheie Străină**: Asigură integritatea datelor prin legarea echipelor de departamente, contractelor de proiecte și directori, și lansărilor de echipe și proiecte.
- **Manipulare Date**: Diverse instrucțiuni `INSERT` populează tabelele cu date inițiale.
- **Interogări și Rapoarte**: Baza de date include interogări complexe pentru a genera rapoarte privind numărul mediu de sarcini pe echipă pe proiect, categorizarea angajaților după salariu și actualizarea înregistrărilor pe baza unor condiții specifice.

## Interogări Personalizate

Mai multe interogări personalizate oferă insight-uri, cum ar fi:
- Numărul mediu de sarcini pentru echipele care lucrează la proiecte specifice.
- Numele angajaților și anii angajării cu formatare modificată.
- Directorii implicați în proiecte la un anumit stadiu de completare.

