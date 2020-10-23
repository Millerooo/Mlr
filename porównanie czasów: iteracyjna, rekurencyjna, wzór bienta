#include <iostream>
#include <math.h>
#include <chrono>
using namespace std;

long long int fib2(long int n) {
    if (n == 0) return 0;
    if (n == 1) return 1;
    return fib2(n - 1) + fib2(n - 2);

}
long long int fib(long int n) {

    return 1.0 / sqrt(5.0) * (pow((1.0 + sqrt(5.0)) / 2.0, (double)(n)) - pow((1.0 - sqrt(5.0)) / 2.0, (double)(n)));
}

long long int fib3(long int n) {
    if ((n == 0) || (n == 1)) return n;
    unsigned int a, b;
    a = 1; b = 1;
    for (unsigned int i = 0; i < n - 2; i++) {
        std::swap(a, b);
        b += a;
    }
    return b;
}

int main()
{
    auto start = std::chrono::high_resolution_clock::now();
    cout << "wynik:" << fib(45);
    auto finish = std::chrono::high_resolution_clock::now();
    std::chrono::duration<double> elapsed = finish - start;
    std::cout << "Elapsed time: " << elapsed.count() << " s\n";

    start = std::chrono::high_resolution_clock::now();
    cout << "wynik2:" << fib2(45);
    finish = std::chrono::high_resolution_clock::now();
    std::chrono::duration<double> elapsed2 = finish - start;
    std::cout << "Elapsed time: " << elapsed2.count() << " s\n";
     start = std::chrono::high_resolution_clock::now();

    cout << "wynik iteracyjny:" << fib3(45);
    finish = std::chrono::high_resolution_clock::now();
    std::chrono::duration<double> elapsed3 = finish - start;
    std::cout << "Elapsed time: " << elapsed3.count() << " s\n";
    start = std::chrono::high_resolution_clock::now();
    return 0;
}
