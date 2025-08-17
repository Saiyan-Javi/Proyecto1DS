---
noteId: "601e7a007bc111f088126d3c4943633f"
tags: []

---

# Libro de Códigos – Establecimientos (Diversificado, v4)

**Estándares de limpieza aplicados:**

- Texto en MAYÚSCULAS y SIN ACENTOS en campos categóricos.

- Guiones internos conservados con espacios estándar (` - `).

- Bullets iniciales removidos en `ESTABLECIMIENTO`/`DIRECCION`.

- `DIRECCION`: abreviaturas expandidas; OCR en `RUTA` (I/L→1, O→0).

- `ZONA`: extraída de dirección y/o dept/muni; `CIUDAD CAPITAL` → `GUATEMALA/GUATEMALA`.

- `DIRECCION_STD` con orden canónico: AVENIDA, CALLE, KM, NUMERO, nominativos, resto.

- Duplicados en capital por posible doble unión (`DUP_CAPITAL_MERGE`, `DUP_CAPITAL_CODIGOS_DISTINTOS`).

- Sin eliminación de filas/columnas; solo marcado/normalización.


**Descripción general:**

- Registros: 6599

- ZONA con valor: 3765 | NA: 2834

- Archivos: `duplicados_capital_merge_v4.csv`, `duplicados_capital_merge_detalle_v4.csv`.


## Variables

### CODIGO
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** 16 - 01 - 0138 - 46, 16 - 01 - 0139 - 46, 16 - 01 - 0140 - 46

### DISTRITO
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** 16 - 031, 16 - 031, 16 - 031

### DEPARTAMENTO
- **Descripción:** Ubicación administrativa normalizada.
- **Ejemplo(s):** ALTA VERAPAZ, ALTA VERAPAZ, ALTA VERAPAZ

### MUNICIPIO
- **Descripción:** Ubicación administrativa normalizada.
- **Ejemplo(s):** COBAN, COBAN, COBAN

### ESTABLECIMIENTO
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** COLEGIO COBAN, COLEGIO PARTICULAR MIXTO VERAPAZ, COLEGIO LA INMACULADA

### DIRECCION
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** KM.2 SALIDA A SAN JUAN CHAMELCO ZONA 8, KM 209.5 ENTRADA A LA CIUDAD, 7A. AVENIDA 11 - 109 ZONA 6

### TELEFONO
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** 77945104, 77367402, 78232301

### SUPERVISOR
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** PATRICIO NAJARRO ASENCIO, PATRICIO NAJARRO ASENCIO, PATRICIO NAJARRO ASENCIO

### DIRECTOR
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** GUSTAVO ADOLFO SIERRA POP, GILMA DOLORES GUAY PAZ DE LEAL, VIRGINIA SOLANO SERRANO

### NIVEL
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** DIVERSIFICADO, DIVERSIFICADO, DIVERSIFICADO

### SECTOR
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** PRIVADO, PRIVADO, PRIVADO

### AREA
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** URBANA, URBANA, URBANA

### STATUS
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** ABIERTA, ABIERTA, ABIERTA

### MODALIDAD
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** MONOLINGUE, MONOLINGUE, MONOLINGUE

### JORNADA
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** MATUTINA, MATUTINA, MATUTINA

### PLAN
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** DIARIO(REGULAR), DIARIO(REGULAR), DIARIO(REGULAR)

### DEPARTAMENTAL
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** ALTA VERAPAZ, ALTA VERAPAZ, ALTA VERAPAZ

### DEPARTAMENTO_ORIGEN
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** AltaVerapaz, AltaVerapaz, AltaVerapaz

### ESTABLECIMIENTO_ORIG
- **Descripción:** Valor original del nombre (antes de limpieza).
- **Ejemplo(s):** COLEGIO COBAN, COLEGIO PARTICULAR MIXTO VERAPAZ, COLEGIO "LA INMACULADA"

### DIRECCION_ORIG
- **Descripción:** Valor original de la dirección (antes de limpieza).
- **Ejemplo(s):** KM.2 SALIDA A SAN JUAN CHAMELCO ZONA 8, KM 209.5 ENTRADA A LA CIUDAD, 7A. AVENIDA 11 - 109 ZONA 6

### TELEFONO_ORIG
- **Descripción:** Valor original del teléfono (antes de extracción).
- **Ejemplo(s):** 77945104, 77367402, 78232301

### TELEFONO_VALIDO
- **Descripción:** Indicador: True si se extrajo al menos un teléfono de 8 dígitos.
- **Ejemplo(s):** True, True, True

### ZONA
- **Descripción:** Zona administrativa (si aplica); NA si no disponible.
- **Ejemplo(s):** 8, 6, 2

### DIRECCION_STD
- **Descripción:** Dirección estandarizada (orden canónico).
- **Ejemplo(s):** KM 2, SALIDA A SAN JUAN CHAMELCO, KM 209.5, ENTRADA A LA CIUDAD, AVENIDA 11, 7A. - 109

### DIR_AVENIDA
- **Descripción:** Componente extraído de la dirección.
- **Ejemplo(s):** 11, 6, 5

### DIR_CALLE
- **Descripción:** Componente extraído de la dirección.
- **Ejemplo(s):** 11, 1, 2

### DIR_KM
- **Descripción:** Componente extraído de la dirección.
- **Ejemplo(s):** 2, 209.5, 209.5

### DIR_NUMERO
- **Descripción:** Componente extraído de la dirección.
- **Ejemplo(s):** 17, 1, 9

### __KEY_MERGE_CAP__
- **Descripción:** Campo de la fuente; normalizado cuando aplica.
- **Ejemplo(s):** COLEGIO COBAN|KM 2, SALIDA A SAN JUAN CHAMELCO|COBAN|ALTA VERAPAZ|MATUTINA|DIARIO(REGULAR)|77945104, COLEGIO PARTICULAR MIXTO VERAPAZ|KM 209.5, ENTRADA A LA CIUDAD|COBAN|ALTA VERAPAZ|MATUTINA|DIARIO(REGULAR)|77367402, COLEGIO LA INMACULADA|AVENIDA 11, 7A. - 109|COBAN|ALTA VERAPAZ|MATUTINA|DIARIO(REGULAR)|78232301

### DUP_CAPITAL_MERGE
- **Descripción:** True si el registro forma parte de un cluster duplicado en la capital (posible doble unión).
- **Ejemplo(s):** False, False, False

### DUP_CAPITAL_CODIGOS_DISTINTOS
- **Descripción:** True si dentro de su cluster hay códigos distintos.
- **Ejemplo(s):** False, False, False
