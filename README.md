# Kavics játék dokumentáció - Mesterséges Intelligencia gyakorlat beadandó II. Kállai Viktor L88I9I

Ez a dokumentáció leírja a megadott programkód különböző osztályait, a megoldó algoritmusok gyorsaságát, és tartalmaz folyamatábrákat a BacktrackSolver és HillClimbSolver osztályokhoz.

## Osztályok

### BacktrackSolver osztály

A BacktrackSolver osztály egy backtracking algoritmust valósít meg, amely rekurzívan próbálja megoldani a játékot. Az osztály a következő attribútumokat és metódusokat tartalmazza:

Attribútumok:
       
- State initialState: A kezdeti állapot.
        
- List<Operator> operators: Az operátorok listája.

Metódusok:
        
- BacktrackSolver(State initialState, List<Operator> operators): Konstruktor, amely beállítja a kezdeti állapotot és az operátorok listáját.
        
- bool Solve(State currentState, Stack<Operator> path): A backtrack algoritmus fő metódusa, amely rekurzívan próbálja megoldani a játékot.

Folyamatábra a BacktrackSolver osztályhoz:

![backtracksolver_beadando2](https://github.com/kallaiviktor/mestintbeadando2ekke/assets/44492387/6e9faaf9-13e3-4a21-91ea-076bfbcce5db)

### HillClimbSolver osztály

A HillClimbSolver osztály egy hill climbing algoritmust valósít meg, amely iteratívan próbálja megoldani a játékot. Az osztály a következő attribútumokat és metódusokat tartalmazza:

Attribútumok:

- State initialState: A kezdeti állapot.

- List<Operator> operators: Az operátorok listája.

Metódusok:

- HillClimbSolver(State initialState, List<Operator> operators): Konstruktor, amely beállítja a kezdeti állapotot és az operátorok listáját.

- void Solve(): A hill climbing algoritmus fő metódusa, amely iteratívan próbálja megoldani a játékot.

Folyamatábra a HillClimbSolver osztályhoz:

![hillclimbsolver_beadando2](https://github.com/kallaiviktor/mestintbeadando2ekke/assets/44492387/699a4982-7430-4911-86bf-1d19309a1c82)

### Operator osztály

Az Operator osztály az egyes operátorokat reprezentálja, amelyek kavicsokat vesznek el a kupacokból. Az osztály a következő attribútumokat és metódusokat tartalmazza:

Attribútumok:

- int TakeFromHeap1: Az első kupacból elveendő kavicsok száma.

- int TakeFromHeap2: A második kupacból elveendő kavicsok száma.

Metódusok:

- Operator(int takeFromHeap1, int takeFromHeap2): Konstruktor, amely beállítja, hogy hány kavicsot veszünk el az egyes kupacokból.

- bool IsValid(State state): Ellenőrzi, hogy az operátor érvényes-e a megadott állapotban.

- State Apply(State state): Alkalmazza az operátort a megadott állapotra, és visszaadja az új állapotot.

### State osztály

A State osztály a játék aktuális állapotát reprezentálja. Az osztály a következő attribútumokat és metódusokat tartalmazza:

Attribútumok:

- int Heap1: Az első kupac kavicsainak száma.

- int Heap2: A második kupac kavicsainak száma.

Metódusok:

- State(int heap1, int heap2): Konstruktor, amely beállítja a kezdeti kavicsok számát mindkét kupacban.

- bool IsTerminal(): Ellenőrzi, hogy az állapot terminális állapot-e (azaz az egyik kupac üres-e).

- override string ToString(): String reprezentáció az állapot könnyű kiírásához.

### Game osztály

A Game osztály kezeli a játék logikáját és a játékosok körét. Az osztály a következő attribútumokat és metódusokat tartalmazza:

Attribútumok:

- State initialState: A kezdeti állapot.

- List<Operator> operators: Az operátorok listája.

Metódusok:

- Game(int heap1, int heap2): Konstruktor, amely beállítja a kezdeti állapotot és generálja az operátorokat.

- List<Operator> GenerateOperators(): Generálja az összes lehetséges operátort a kezdeti állapot alapján.

- void Play(): A játék fő metódusa, amely kezeli a játékosok körét és a játék állapotát.

## Megoldó algoritmusok gyorsasága

### BacktrackSolver algoritmus

A backtracking algoritmus rekurzívan próbálja megoldani a játékot minden lehetséges operátor alkalmazásával. Ez az algoritmus nagyon alapos, de a legrosszabb esetben exponenciális időbonyolultságú lehet, mivel minden lehetséges állapotot végigpróbál.

### HillClimbSolver algoritmus

A hill climbing algoritmus iteratívan próbálja megoldani a játékot, mindig a legjobb operátort választva. Ez az algoritmus gyorsabb lehet, mivel nem próbál meg minden lehetséges állapotot, hanem csak a legjobbnak tűnő irányba halad. Azonban nem garantálja a globális optimum elérését, mivel lokális maximumokba ragadhat.














