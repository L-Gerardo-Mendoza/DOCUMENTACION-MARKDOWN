### Ejercicio 1: Identificación de matrices y suma de matrices

#### Enunciado del Problema Original

1. Identificar el tipo de la siguiente matriz:

\[
A = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
\]

2. Calcular la suma de las matrices \(A\) y \(B\):

\[
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix},
\quad
B = \begin{pmatrix}
9 & 10 & 11 \\
12 & 13 & 14
\end{pmatrix}
\]

#### Solución o Respuesta

1. La matriz \(A\) es una **matriz identidad**, porque:
   - La diagonal principal está compuesta solo por **unos**.
   - Todos los elementos fuera de la diagonal son **ceros**.

2. La suma \(A + B\) es:

\[
A + B =
\begin{pmatrix}
10 & 12 & 14 \\
16 & 18 & 20
\end{pmatrix}
\]

#### Proceso / Procedimiento

1. **Identificación de la matriz identidad**
   1. Revisar la **diagonal principal** de \(A\): los elementos son 1 y 1.
   2. Verificar que todos los elementos **fuera** de la diagonal sean 0.
   3. Conclusión: cumple la definición de matriz identidad \(I_2\).

2. **Suma de matrices \(A + B\)**
   1. Verificar que \(A\) y \(B\) tengan **las mismas dimensiones** (2×3).
   2. Sumar **elemento a elemento**:

      - Primera fila:
        - \(1 + 9 = 10\)
        - \(2 + 10 = 12\)
        - \(3 + 11 = 14\)
      - Segunda fila:
        - \(4 + 12 = 16\)
        - \(5 + 13 = 18\)
        - \(6 + 14 = 20\)

   3. Escribir la matriz resultado:

      \[
      A + B =
      \begin{pmatrix}
      10 & 12 & 14 \\
      16 & 18 & 20
      \end{pmatrix}
      \]

#### Código (opcional en JavaScript)

```javascript
function sumarMatrices(A, B) {
  const filas = A.length;
  const columnas = A[0].length;
  const resultado = [];

  for (let i = 0; i < filas; i++) {
    const fila = [];
    for (let j = 0; j < columnas; j++) {
      fila.push(A[i][j] + B[i][j]);
    }
    resultado.push(fila);
  }
  return resultado;
}
