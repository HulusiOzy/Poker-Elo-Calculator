# Poker ELO Calculator

Just a simple ELO calculator for poker games between you and your friends.

> **Note:** Do note that all ELOs must be set to 1000 (or whatever starting ELO you have chosen) before every use.

## Main Formula

The main formula used is:

\`\`\`
Rnew = Rold + K(S - E)
\`\`\`

- \`K\` is the scalar. For this, it's kept at 100.
- \`S\` is the score outcome of each game.
- \`E\` is their expected win percentage, taking their ELO into account.

## Scoring System

The score \`S\` is calculated by getting the number of players, floor dividing it by 2, and anyone who has a position below that number gets a score of \`1/N\`, where \`N\` is their position.

**Example:** If the player count is 7, \`7 // 2\` is 3. Anyone with a score of 1, 2, or 3 gets a score of \`1/1\`, \`1/2\`, or \`1/3\`, respectively.

## Expected Win Percentage

The expected win percentage \`E\` is calculated using the following formula:

\`\`\`
E = Rplayer / (Rplayer + Ropponent1 + Ropponent2 + ... + RopponentN)
\`\`\`

Where \`Rplayer\` is the ELO rating of the player, and \`Ropponent1\`, \`Ropponent2\`, ..., \`RopponentN\` are the ELO ratings of the opponents.
