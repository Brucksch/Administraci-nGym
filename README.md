# TFI - Administración de Gimnasio (Java por consola)

Proyecto minimalista para Programación II (UTN TUP). Cumple con:
- CRUD de Socios
- POO (clases, enum, interfaces funcionales)
- Colecciones (ArrayList, HashMap)
- TAD propio (lista enlazada simple para bitácora)
- Arrays (altas por mes)
- Excepción propia
- Streams, lambdas, method references
- Menú por consola con `Scanner`, `switch`, `do/while`

## Requisitos
- Java 17+
- Maven 3.8+

## Cómo ejecutar
```bash
mvn -q -e -DskipTests package
mvn -q exec:java
```
o desde IntelliJ: **Add Configuration → Maven → exec:java** (Main: `tfi.app.Main`).

## Estructura
```
src/main/java/tfi
 ├─ app/Main.java
 ├─ domain/{Socio, Plan, Identificable, Pagable}.java
 ├─ service/GimnasioService.java
 ├─ util/OperacionLog.java        # lista enlazada propia
 └─ exception/SocioNoEncontradoException.java
```

## Flujo de Git sugerido
1. Crear el repo y subir `main`/`develop`.
2. Cada integrante trabaja en su rama (`rama-juan`, `rama-ana`).
3. Features chicas (`feature/alta-socio`, `feature/cambiar-plan`), commits descriptivos.
4. Pull Request a `develop` → revisión → merge.
5. Tag de versiones (`v0.1`, `v0.2`).
6. En `README.md` registrar aportes por integrante.

## Notas
- `calcularCuota()`: 10% de descuento si la antigüedad >= 12 meses.
- `altasPorMes`: contador simple (array de 12).
- Bitácora: lista enlazada propia (`OperacionLog`).
