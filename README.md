# Poker-Elo-Calculator
Just a simple ELO calculator for poker between me and my friends
The main formula used is
Rnew = Rold + K(S - E)
K is the scalar. For this I keep it at 100
S is the Score outcome of each game
S is calculated by getting the number of players, floor dividing it by 2 and anyone who has a position below that number get a score of 1/N. N being their position.
EXAMPLE: If the player count is 7, 7//2 is 3. Anyone with a score of 1/2/3 get a score of either 1/1, 1/2 or 1/3.
E is their expected win % getting their elo into account.
The formula simply is: E = Rplayer / (Rplayer + Ropponent1 + Ropponent2 + ... + RopponentN)
