# Vlastní kategorie příkladů

Tato sekce popisuje, jak do vlastní instance LingeBota přidat vlastní kategorie pro [generaci příkladů](../02HlavniInstance/2generate.md). Vyžaduje se znalost programovacího jazyka Python.

Každá kategorie příkladu odpovídá jednomu modulu v balíku `problems`, který se nachází v podadresáři `utils/problem_utils/` (kromě modulu `__init__.py`):

![h](../img/040401.png)

Obsah modulů musí splňovat určitá pravidla a pro přidání kategorie do bota je ještě potřeba několik dalších kroků. Proto bude postup ukázán na jednoduchém příkladu, kdy je přidána kategorie pro malou násobilku:

## [1] Vytvoření modulu

__1.1.__ Vytvořte v balíku `problems` nový Python modul `basic_multiplication.py`. Jméno souboru nemá vliv na výsledný název kategorie.

![h](../img/040402.png)

__1.2.__ V modulu naimportujte třídu `GeneralProblem` a definujte třídu `Problem`, která ze třídy `GeneralProblem` dědí.

__1.3.__ Definujte magickou metodu `__str__`, která vrací řetězec _Malá násobilka_. Obsah řetězce určuje, jak se bude kategorie jmenovat.

__1.4.__ Definujte metodu `generate_problem` a zatím ji nechte prázdnou.

```py
from utils.problem_utils.problem_utils import GeneralProblem


class Problem(GeneralProblem):
    def __str__(self) -> str:
        return "Malá násobilka"

    def generate_problem(self) -> None:
        pass
```

## [2] Zaregistrování modulu

__2.1.__ Do kolekce `__all__` v modulu `__init__.py` z balíku `problems` přidejte položku `"basic_multiplication"`. Jedná se o řetězec obsahující název nově vytvořeného modulu. Na pořadí položek v kolekci nezáleží.

```py
__all__ = [
    "matrix_multiplication",
    "gauss_jordan",
    "inverse_matrix",
    "eigen",
    "determinant",
    "gram_schmidt",
    "basic_multiplication"
]
```

__2.2__ Do kolekce `__problems_list__` v modulu `utils/problem_utils/problem_manager.py` přidejte položku `basic_multiplication.Problem()`. Jedná se o třídu definovanou v kroku 1. Pořadí položek v této kolekci určuje pořadí položek ve výběrovém seznamu po zadání příkazu `/generate`.

```py
problems_list: list[GeneralProblem] = [
    matrix_multiplication.Problem(),
    gauss_jordan.Problem(),
    inverse_matrix.Problem(),
    eigen.Problem(),
    determinant.Problem(),
    gram_schmidt.Problem(),
    basic_multiplication.Problem()
]
```

__2.3.__ Kategorie je nyní vidět ve výběrovém seznamu a lze ji zvolit. Generování příkladů ale nic nedělá, to protože tělo metody `generate_problem` je prázdné.

![h](../img/040403.png)

## [3] Definice logiky generace příkladů

__3.1.__ Vraťte se do modulu `basic_multiplication.py` z balíku `problems`.

__3.2.__ V metodě `generate_problem` do proměnných `self.task` a `self.answer` uložte text zadání a text řešení vygenerovaného příkladu.
