void main() {
  // Lista de 10 números
  List<int> numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

  // Calculando la suma de la lista
  int suma = numeros.reduce((a, b) => a + b);

  // Calculando la suma de los pares e impares
  int sumaPares = numeros.where((n) => n % 2 == 0).reduce((a, b) => a + b);
  int sumaImpares = numeros.where((n) => n % 2 != 0).isNotEmpty
      ? numeros.where((n) => n % 2 != 0).reduce((a, b) => a + b)
      : 0;

  // Hallando el número mayor y el menor
  int maxNumero = numeros.reduce((a, b) => a > b ? a : b);
  int minNumero = numeros.reduce((a, b) => a < b ? a : b);

  // Imprimiendo resultados
  print('La suma de la lista es: $suma');
  print('La suma de los números pares es: $sumaPares');
  print('La suma de los números impares es: $sumaImpares');
  print('El número mayor es: $maxNumero');
  print('El número menor es: $minNumero');
}
