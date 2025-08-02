// calculadora.cpp (Versión con función de potencia)
#include <iostream>
#include <cmath>
using namespace std;

double sumar(double a, double b) {
    return a + b;
}

double restar(double a, double b) {
    return a - b;
}

double multiplicar(double a, double b) {
    return a * b;
}

double dividir(double a, double b) {
    if (b == 0) {
        cout << "Error: División por cero no permitida." << endl;
        return 0;
    }
    return a / b;
}

double potencia(double base, double exponente) {
    return pow(base, exponente);
}

double logaritmo( double a) {  // funcion para logatirmo//
    if (a <=0) {
        cout<< "Error: Logaritmo de numero negativo o cero no permitido." << endl;
        return 0;
    }
    return log10(a); // logaritmo en base 10//

}

int main() {
    double num1, num2;
    char operacion;
    cout << "Ingrese dos números: ";
    cin >> num1 >> num2;
    cout << "Ingrese operación (+, -, *, /, ^, l): ";
    cin >> operacion;

    switch (operacion) {
        case '+':
            cout << "Resultado: " << sumar(num1, num2) << endl;
            break;
        case '-':
            cout << "Resultado: " << restar(num1, num2) << endl;
            break;
        case '*':
            cout << "Resultado: " << multiplicar(num1, num2) << endl;
            break;
        case '/':
            cout << "Resultado: " << dividir(num1, num2) << endl;
            break;
        case '^':
            cout << "Resultado: " << potencia(num1, num2) << endl;
            break;
        default:
            cout << "Operación no válida." << endl;
            break;
        case 'l':
            cout << "resultado: " << logaritmo (num1) << endl; // logaritmo de num1//
            break;
        default:
            cout << "operacion no admitida."<< endl;
    }
    return 0;
}
