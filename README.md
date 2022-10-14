# Dagger 2 vs Koin vs Kodein vs Katana

The project is based on Android Injection Performance (https://github.com/Sloy/android-dependency-injection-performance). 

All libraries have been updated to the latest versions. 

Updated gradle and included support for android x.


## Libraries tested
- [Koin](https://insert-koin.io/) - 3.1.2
- [Kodein](http://kodein.org/Kodein-DI/) - 6.3.3
- [Dagger 2](https://google.github.io/dagger/) - 2.44
- [Katana](https://github.com/rewe-digital-incubator/katana/) - 1.15.0
 
 
## The test
The test data are classes with dependencies in a structure similar to Fibonacci sequence, to simulate multiple levels of transitive dependencies.
For each library there is a test with Kotlin classes and one with Java classes, because some libraries seem to be affected by this difference.

Each test injects one of this dependencies 100 times and prints the maximum time, the minimum and the average.

The project contains an Android application that run the tests on its onCreate and prints the result to the Logcat.

The actual test is implemented in the class [InjectionTest.kt]


Library | Setup Kotlin | Setup Java | Inject Kotlin | Inject Java
--- | ---:| ---:| ---:| ---:
**Koin** | 0.22 ms | 0.21 ms  | 0.10 ms | 0.10 ms
**Dagger** | 0.01 ms | 0.00 ms  | 0.04 ms | 0.03 ms
**Custom** | 0.04 ms | 0.04 ms  | 0.03 ms | 0.05 ms
**Kodein** | 2.79 ms | 2.82 ms  | 0.13 ms | 0.10 ms
**Katana** | 0.21 ms | 0.18 ms  | 0.07 ms | 0.05 ms
