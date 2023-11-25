% Facts representing family relationships
male(john).
male(mike).
male(tom).
male(jerry).
male(harry).

female(susan).
female(lily).
female(lisa).
female(sarah).

parent(john, mike).
parent(john, lily).
parent(susan, mike).
parent(susan, lily).
parent(mike, tom).
parent(lily, jerry).
parent(lily, sarah).
parent(tom, harry).
parent(lisa, harry).

% Rules to define specific family relationships
father(Father, Child) :-
    male(Father),
    parent(Father, Child).

mother(Mother, Child) :-
    female(Mother),
    parent(Mother, Child).

% Rules to define siblings and grandparents
sibling(Sibling1, Sibling2) :-
    parent(Parent, Sibling1),
    parent(Parent, Sibling2),
    Sibling1 \= Sibling2.

grandparent(Grandparent, Grandchild) :-
    parent(Grandparent, Parent),
    parent(Parent, Grandchild).

% Example queries:
% To find all children of John:
% ?- parent(john, Child).
% This will return all children of John (Mike and Lily).

% To find all grandchildren of Susan:
% ?- grandparent(susan, Grandchild).
% This will return all grandchildren of Susan (Tom, Jerry, and Sarah).

% To check if Mike and Lily are siblings:
% ?- sibling(mike, lily).
% This will return true.

% To find the father of Tom:
% ?- father(Father, tom).
% This will return the father of Tom (Mike).

% To find the mother of Harry:
% ?- mother(Mother, harry).
% This will return the mother of Harry (Lisa).
