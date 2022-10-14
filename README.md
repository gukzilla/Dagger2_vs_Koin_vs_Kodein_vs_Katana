# Dagger 2 vs Koin vs Kodein vs Katana

The project is based on Android Injection Performance (https://github.com/Sloy/android-dependency-injection-performance). 

All libraries have been updated to the latest versions. 

Updated gradle and included support for android x.

 
 
Проект базируется на Android Injection Performance (https://github.com/Sloy/android-dependency-injection-performance). 

Были обновлены все библиотеки до актуальных версий. 

Обновлены градл и включена поддержка андроид х.

## Тест

Library | Setup Kotlin | Setup Java | Inject Kotlin | Inject Java
--- | ---:| ---:| ---:| ---:
**Koin** | 0.22 ms | 0.21 ms  | 0.10 ms | 0.10 ms
**Dagger** | 0.01 ms | 0.00 ms  | 0.04 ms | 0.03 ms
**Custom** | 0.04 ms | 0.04 ms  | 0.03 ms | 0.05 ms
**Kodein** | 2.79 ms | 2.82 ms  | 0.13 ms | 0.10 ms
**Katana** | 0.21 ms | 0.18 ms  | 0.07 ms | 0.05 ms
