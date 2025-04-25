Hello, to solve this exercice, you could for example use a ternary expression like this :

```c++

#include "collatz_conjecture.h"
#include <stdexcept>

namespace collatz_conjecture {

    int steps(int number) {

        if (number <= 0) {
            throw std::domain_error("Only positive numbers are allowed!");
        }

        int steps = 0;

        while (number != 1) {
            number = number % 2 == 0 ? number / 2 : number * 3 + 1; // You can use if-else too, but it is less concise
            ++ steps; 
        }

        return steps;

    }

}  // namespace collatz_conjecture

```

Good luck !
