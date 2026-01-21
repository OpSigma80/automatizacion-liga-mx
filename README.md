<img width="1432" height="741" alt="image" src="https://github.com/user-attachments/assets/ca9675f4-1d5c-4df8-8989-68187469b6df" />

# 🏆 Sistema de Gestión Liga MX

Sistema automatizado en Python para gestionar la tabla de posiciones de la Liga MX usando Excel.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![OpenPyXL](https://img.shields.io/badge/OpenPyXL-3.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Características

- ✅ Tabla de 18 equipos de Liga MX
- ✅ Registro automático de resultados
- ✅ Actualización de estadísticas (PJ, PG, PE, PP, GF, GC, DIF, Puntos)
- ✅ Ordenamiento automático por puntos
- ✅ Historial de partidos por jornada
- ✅ Validaciones y manejo de errores
- ✅ Evita duplicados automáticamente
- ✅ Interfaz de consola con emojis

## 🚀 Instalación

### Requisitos previos
- Python 3.8 o superior
- pip o pipenv

### Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/automatizacion-liga-mx.git
cd automatizacion-liga-mx
```

### Instalar dependencias

**Opción 1: Con pipenv (recomendado)**
```bash
pipenv install
```

**Opción 2: Con pip**
```bash
pip install openpyxl
```

## 💻 Uso

### Ejecución básica

**Con pipenv:**
```bash
pipenv run python excel-03.py
```

**Con python:**
```bash
python excel-03.py
```

Esto creará un archivo `Liga_MX.xlsx` con:
- **Hoja 1:** Tabla de Posiciones (ordenada automáticamente)
- **Hoja 2:** Resultados por jornada

### Ejemplo de salida en consola

```
📁 Creando nuevo archivo de Liga MX...
✅ Archivo 'Liga_MX.xlsx' creado exitosamente
📊 18 equipos registrados

==================================================
REGISTRANDO RESULTADOS - JORNADA 1
==================================================

⚽ JORNADA 1
==================================================
América 2 - 1 Guadalajara
==================================================
🏠 América: Victoria (+3 puntos)
✈️  Guadalajara: Derrota (+0 puntos)

==========================================================================================
                              TABLA DE POSICIONES - LIGA MX
==========================================================================================
Pos   Equipo               PJ    PG    PE    PP    GF    GC    DIF    Pts
------------------------------------------------------------------------------------------
1     América              1     1     0     0     2     1     1      3
2     Cruz Azul            1     1     0     0     3     0     3      3
...
```

## 📊 Funciones principales

### `crear_archivo_nuevo()`
Crea un archivo Excel nuevo con la estructura de la Liga MX y los 18 equipos registrados.

### `registrar_resultado(jornada, equipo_local, goles_local, goles_visitante, equipo_visitante)`
Registra el resultado de un partido y actualiza automáticamente las estadísticas.

**Parámetros:**
- `jornada` (int): Número de jornada (1-17)
- `equipo_local` (str): Nombre del equipo local
- `goles_local` (int): Goles anotados por el equipo local
- `goles_visitante` (int): Goles anotados por el equipo visitante
- `equipo_visitante` (str): Nombre del equipo visitante

**Ejemplo:**
```python
registrar_resultado(1, 'América', 2, 1, 'Guadalajara')
```

### `agregar_equipo(nombre_equipo)`
Agrega un nuevo equipo a la tabla (evita duplicados automáticamente).

**Ejemplo:**
```python
agregar_equipo('Atlante')
```

### `mostrar_tabla()`
Muestra la tabla de posiciones actualizada en la consola.

### `obtener_equipos()`
Retorna una lista con todos los equipos registrados.

## 🛡️ Validaciones implementadas

- ✅ Verifica que los equipos existan antes de registrar un partido
- ✅ No permite equipos duplicados
- ✅ Valida que los goles sean números enteros positivos
- ✅ Manejo de errores con try-except
- ✅ Mensajes informativos de error

## 🏅 Sistema de puntos

- **Victoria:** +3 puntos
- **Empate:** +1 punto (para ambos equipos)
- **Derrota:** 0 puntos

## 📖 Criterios de desempate

La tabla se ordena por:
1. **Puntos** (mayor a menor)
2. **Diferencia de goles** (mayor a menor)
3. **Goles a favor** (mayor a menor)

## 📁 Estructura del proyecto

```
automatizacion-liga-mx/
├── excel-03.py              # Código de producción (versión limpia)
├── excel-03-explicado.py    # Código con comentarios educativos
├── README.md                # Este archivo
├── Pipfile                  # Dependencias de pipenv
├── .gitignore              # Archivos ignorados por git
└── Liga_MX.xlsx            # Archivo generado (no incluido en git)
```

## 🎓 Aprendizaje

Si quieres entender cómo funciona el código línea por línea, revisa `excel-03-explicado.py` que incluye:
- Comentarios detallados en cada función
- Explicación de conceptos de Python
- Explicación de conceptos de OpenPyXL
- Buenas prácticas de programación

## 🔧 Personalización

### Cambiar equipos iniciales
Edita la lista `equipos` en la función `crear_archivo_nuevo()`:

```python
equipos = [
    'Tu Equipo 1', 'Tu Equipo 2', ...
]
```

### Cambiar nombre del archivo
Modifica la constante al inicio del archivo:

```python
archivo = 'Tu_Archivo.xlsx'
```

### Personalizar estilos
Los colores y estilos se pueden modificar en `crear_archivo_nuevo()`:

```python
celda.fill = PatternFill(start_color="TU_COLOR_HEX", ...)
```

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea tu rama de características (`git checkout -b feature/CaracteristicaIncreible`)
3. Commit tus cambios (`git commit -m 'Add: nueva característica'`)
4. Push a la rama (`git push origin feature/CaracteristicaIncreible`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto es de código abierto bajo la licencia MIT.

## 👨‍💻 Autor

**Tu Nombre**
- GitHub: [OpSigma80](https://github.com/OpSigma80)
- LinkedIn: [Israel Sanchez Rovira](https://www.linkedin.com/in/israel-sanchez-rovira)

## 🙏 Agradecimientos

- Comunidad de Python
- Documentación de OpenPyXL
- Liga MX por la inspiración

---

⭐ **Si te gustó este proyecto, dale una estrella en GitHub!**

📧 **¿Preguntas o sugerencias?** Abre un [Issue](https://github.com/tu-usuario/automatizacion-liga-mx/issues)
