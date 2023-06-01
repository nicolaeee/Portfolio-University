---
title: Sturucture C++/C
----
#  C++ Structures (struct)
Structures (also called structs) are a way to group several related variables into one place. Each variable in the structure is known as a member of the structure.

Unlike an array, a structure can contain many different data types (int, string, bool, etc.).

```

#include <iostream>
using namespace std;
int main()
{
	//Create my first struct which contains some info about some person:
	struct pers
	{
		char num[15];
		string pren;
		int nr_cop;
	};
	pers p1, p2;//Variable of sturucture some sorf of an object
	cout << "Nume: "; cin >> p1.num;
	cout << " Prenume :"; cin >> p1.pren;
	cout << "Nr de copilasi: "; cin >> p1.nr_cop;

	//Information about first person:
	cout << "Info despre persoana numarul 1: "<<'\n';
	cout << p1.num << " " << p1.pren << " " << p1.nr_cop;

	p2 = p1;

	//new variable of structure:
	pers p3 = { "Ion", "Gorobet", 4 };

	//Outputing with pointers
	pers* p;
	p = &p3;
	cout << "Info despre persona numarul 3 prin afisare indirecta cu pointeri:\n'";
	cout << p->num << " " << p->pren << " " << p->nr_cop << endl;

	//Outputing each value in structure with index of an array
	pers array[3];
	array[0] = p1;
	array[1] = p2;
	array[2] = p3;

	for (int i = 0; i < 3; i++) {
		cout << "Array: [" << i << "]= " << array[i].num << " " << array[i].pren << " " << array[i].nr_cop;
	}

}

```