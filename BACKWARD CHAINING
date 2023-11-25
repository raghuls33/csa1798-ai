% Define facts and rules
parent(john, bob).
parent(john, lisa).
parent(mary, lisa).
parent(mary, bob).
male(john).
female(mary).

% Rules for inferring relationships
father(X, Y) :-
    parent(X, Y),
    male(X).

mother(X, Y) :-
    parent(X, Y),
    female(X).

% Backward chaining inference
ancestor(X, Y) :-
    parent(X, Y). % Base case: X is a direct parent of Y

ancestor(X, Y) :-
    parent(X, Z),
    ancestor(Z, Y). % Recursively find ancestors
