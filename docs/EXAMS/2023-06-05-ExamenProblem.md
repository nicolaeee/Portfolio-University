---
title: Teorie Examen
author: Gorobet Nicolae
---

# First Problem

Parantezele rotunde trebuie înlocuite cu acolade {} în declarația și definiția clasei "complex".
După fiecare declarație de membru (variabilă), trebuie adăugată o virgulă ,.
Constructorul clasei "complex" a fost declarat cu tip întreg (int), dar trebuie să fie de tip void.
În definirea constructorului, valorile argumentelor sunt atribuite greșit membrilor a și b, ar trebui să fie a = n1 și b = n2.
În funcția main, parantezele rotunde trebuie înlocuite cu acolade {}.
Operatorul de inserție << nu este supraincarcat pentru clasa "complex", astfel încât nu poate fi utilizat pentru a afișa obiectele x și y.

```
#include <iostream>
using namespace std;

class complex {
private:
    double a, b;

public:
   complex::complex(int n1, int n2) {
    a = n1;
    b = n2;
}

    friend ostream& operator<<(ostream& os, const complex& obj) {
        os << obj.a << " + " << obj.b << "i";
        return os;
    }
};

int main() {
    complex x(40, 3), y(0, 0);
    cout << x << " " << y << endl;
    return 0;
}

```

# Second Problem

În declarația clasei "punct", parantezele trebuie înlocuite cu acolade {}.
Lipsește punct și virgulă (;) după declararea membrilor a și b în clasă.
În definirea constructorului punct, variabila b2 nu este declarată corect, ar trebui să fie a2.
Definiția funcției afis() nu corespunde cu declarația, deoarece funcția a fost declarată ca int în loc de void.
În funcția main, apelul funcției afis() pentru obiectul x conține un spațiu în plus între x și .afis().
Funcția afis() nu returnează nimic, așa că ar trebui să fie de tip void și nu int


```
#include <iostream>
using namespace std;

class punct {
private:
    double a, b;

public:
    punct(double, double);
    void afis();
};

punct::punct(double a1, double b1) {
    a = a1;
    b = b1;
}

void punct::afis() {
    cout << "Punct: " << a << ", " << b << "\n";
}

int main() {
    punct x(40, 7), y;
    x.afis();
    return 0;
}
```