program DiagonalAverage;

var
  A: array[1..10, 1..10] of integer;  // Матриця розміру 10x10
  i, n, j: integer;
  sum, count: integer;
  avg: real;

begin
  // Введення розміру матриці (для прикладу беремо квадратну матрицю 3x3)
  Write('Введіть розмірність матриці n (макс. 10): ');
  ReadLn(n);

  // Введення елементів матриці
  WriteLn('Введіть елементи матриці:');
  for i := 1 to n do
    for j := 1 to n do

      Read(A[i, j]);

  // Обчислення середнього арифметичного головної діагоналі
  sum := 0;
  count := 0;
  
  for i := 1 to n do
  begin
    sum := sum + A[i, i];  // Сума елементів головної діагоналі
    count := count + 1;     // Лічильник елементів на діагоналі
  end;

  // Обчислення середнього арифметичного
  avg := sum / count;

  // Виведення результату
  WriteLn('Середнє арифметичне елементів головної діагоналі: ', avg:0:2);
end.

