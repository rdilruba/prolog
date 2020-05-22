# Project Definition
The project is aim to write Prolog predicates (statements) for manipulating lists of football teams,
and the matches played between them. First predicate is allTeams(L,N). L is the list
containing all the teams in the database where N is the number of elements in the list. In
this predicate, one should be able to specify queries with any combination of variables and
constants like this as an example:
allteams([galatasaray, realmadrid, juventus, kobenhavn, manutd, realsociedad, shaktard,
bleverkusen, omarseille, bdortmund, arsenal, fcnapoli], N).
N = 12.
The predicates related to match results are:
* wins(T,W,L,N) implies that L involves the teams defeated by team T when we are in
week W and N is the number of elements in L.
* losses(T,W,L,N) implies that L involves the teams that defeated team T when we are
in week W and N is the number of elements in L.
* draws(T,W,L,N) is very similar but now L involves the teams that team T could not
defeat also did not lose to.
In that predicates, T and W will be given as constants. Note that, week W means there have
been W matches played by a team. So one should consider all these matches played by the
queried team.
The predicates related to goal numbers are:
* scored(T,W,S) where S is the total number of goals scored by team T up to (and
including) week W.
* conceded(T,W,C) where C is the total number of goals conceded by team T up to
week W.
* average(T,W,A) where A is the average (goals scored { goals conceded) of a team T
gathered up to (and including) week W.
Assume T and W are given as constants.
The other two predicates are:
* order(L,W) where W (week) is given as constant and league order in that week will be
retrieved in L.
* topThree([T1,T2, T3],W) where T1 T2 and T3 are the top teams when we are in the
given week W.
Assuming that the order is decided according to average i.e the one with the highest average
will be at the top. If the two teams have the same average then the order can be in any
order.

# Input & Output

The format of the input and output in this project are predicates, lists,variables, and ‘true
or false’. Inputs are predicates which are goals of user. Prolog’s outputs are results of
these goals.
Examples;

?- wins(galatasaray,4,L,N).

L=[kobenhavn],

N= 1,

false.


?- scored(juventus,5,S).

9,

true,

false.


?- draws(galatasaray,4,[juventus],1).

true,

false.
