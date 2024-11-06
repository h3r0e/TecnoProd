
Esquema de una entidad bancaria

![[Pasted image 20241017083342.png]]

* ***Intersección de conjuntos**

r ∩ s = r − (r − s)

* Ejemplo:
Tots els clients amb un prestec concedit i un compte obert:

ΠNomClient(PRESTATARI) ∩ ΠNomClient(IMPOSITOR)

| **Impositor**  |               |
| -------------- | ------------- |
| **Nom Client** | **NomCompte** |
| Carles         |               |
| Andrea         |               |
| Carla          |               |

| **Prestatari** |                    |
| -------------- | ------------------ |
| **NomClient**  | **NumeroPrestect** |
| Andrea         |                    |
| Alejandra      |                    |
| Marc           |                    |

* ***Reunió natural**

Combinación de operaciones de selección y producto cartesiano.

La reunió natural de r i s, és una relació de l’esquema 
R ∪ S definida com: 

![[Pasted image 20241017083945.png]]

On R ∩ S = A1, A2, ..., An.

* Ejemplo:
El nom de totes les sucursals amb clients que tenen un compte obert i viuen a Peguerinos: 

![[Pasted image 20241017084104.png]]

