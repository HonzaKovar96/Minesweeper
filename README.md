# Minesweeper
Tento kód implementuje hru "Minesweeper" (Miny). Hra se hráči zobrazí jako hrací pole s několika minami skrytými na některých místech pole. Hráč se snaží odkrýt všechna místa na hracím poli, kromě těch s minami, aby vyhrál hru. Pokud hráč odkryje místo s minou, prohrál hru.

Nyní přistupme k jednotlivým funkcím v kódu:

    Board.__init__(self, dim_size, num_bombs): konstruktor třídy Board inicializuje hrací pole o rozměru dim_size x dim_size s počtem min num_bombs. Vytvoří se prázdné hrací pole, náhodně umístí num_bombs min a přiřadí se hodnota pro každé pole na hracím poli, která udává počet min v okolí. Vytvoří se také prázdná množina dug pro pozice, které již hráč odkryl.

    Board.make_new_board(self): tato metoda vytváří nové prázdné hrací pole.

    Board.assign_values_to_board(self): tato metoda přiřazuje každému poli na hracím poli počet min v jeho okolí.

    Board.get_num_neighboring_bombs(self, row, col): tato metoda vrací počet min v okolí daného pole.

    Board.dig(self, row, col): tato metoda odkryje pole na pozici (row, col) a rekurzivně odkryje všechna sousední pole, která nemají minu v okolí. Vrací False, pokud hráč odkryl pole s minou, jinak vrací True.

    Board.__str__(self): metoda, která vrací textovou reprezentaci hracího pole pro zobrazení hráči.

    play(dim_size=10, num_bombs=10): funkce, která inicializuje hrací pole a spustí hru. V průběhu hry se zobrazuje hrací pole a hráč zadává pozice, které chce odkrýt. Pokud hráč odkryje pole s minou, hra končí a hráč prohrál. Pokud hráč úspěšně odkryje všechna pole bez min, hra končí a hráč vyhrál.

Celý kód je napsán v jazyce Python. Pro zobrazení hracího pole je použita metoda __str__(). Hra probíhá v konzolovém rozhraní, kde hráč zadává pozice, které chce odkrýt. Kód také obsahuje ošetření vstupu od hráče
