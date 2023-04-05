Table HTML goes here.

<div id='tables-begin'></div>

| Title                                        | Developer                           | Publisher         | Release Date | Desc                                                                         | Play                                                                                                                          |
| -------------------------------------------- | ----------------------------------- | ----------------- | ------------ | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [[gamerecs/Tetris.md\|Tetris]]               | Bullet-Proof Software               | Nintendo          | 1989-06-14   | Line up falling blocks into complete rows to keep the well from overflowing. | Plenty of options                                                                                                             |
| [[gamerecs/Super Metroid.md\|Super Metroid]] | Nintendo R&D 1, Intelligent Systems | Nintendo          | 1994-03-19   | Samus searches the planet Zebes for an infant Metroid.                       | Switch                                                                                                                        |
| [[gamerecs/Spelunky.md\|Spelunky]]           | Mossmouth                           | Mossmouth         | 2008-12-21   | A spelunker jumps through deadly, procedurally-generated caves.              | [Steam](https://store.steampowered.com/app/239350/Spelunky/) or [GOG](https://www.gog.com/game/spelunky)                      |
| [[gamerecs/Celeste.md\|Celeste]]             | Maddy Makes Games                   | Maddy Makes Games | 2018-01-25   | Face your doubts and climb a mountain in this precise platformer.            | [Steam](https://store.steampowered.com/app/504230/Celeste/) or [Switch](https://www.nintendo.com/games/detail/celeste-switch) |




<div id='tables-end'></div>

JavaScript code goes next.

<script>
$(document).ready( function () {

    // $('#myTable').DataTable();

    $('#tables-begin').nextUntil('#tables-end', 'table').DataTable();

} );
</script>