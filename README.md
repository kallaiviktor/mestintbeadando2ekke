# Kavics játék dokumentáció - Mesterséges Intelligencia gyakorlat beadandó II. Kállai Viktor L88I9I

Ez a dokumentáció leírja a megadott programkód különböző osztályait, a megoldó algoritmusok gyorsaságát, és tartalmaz folyamatábrákat a BacktrackSolver és HillClimbSolver osztályokhoz.

## Osztályok

### BacktrackSolver osztály

A BacktrackSolver osztály egy backtracking algoritmust valósít meg, amely rekurzívan próbálja megoldani a játékot. Az osztály a következő attribútumokat és metódusokat tartalmazza:

    Attribútumok:
        State initialState: A kezdeti állapot.
        List<Operator> operators: Az operátorok listája.

    Metódusok:
        BacktrackSolver(State initialState, List<Operator> operators): Konstruktor, amely beállítja a kezdeti állapotot és az operátorok listáját.
        bool Solve(State currentState, Stack<Operator> path): A backtrack algoritmus fő metódusa, amely rekurzívan próbálja megoldani a játékot.



