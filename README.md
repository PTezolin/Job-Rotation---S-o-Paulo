# Job Rotation - São Paulo

# 2) Dado a sequência de Fibonacci
Onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE: Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;

  print("-----------------------------------------------------------------")
  print("      Verificador de pertencimento à sequência de Fibonacci      ")
  print("-----------------------------------------------------------------")

  while True:
      num_str = input("Informe o número que você deseja verificar ou digite 0 para sair: ")

      if num_str == "0":
          print("Programa encerrado!\n")
          break

      try:
          num_float = float(num_str)
          num_int = int(num_float)
          if num_int != num_float:
              print("Valor inválido. O número deve ser um inteiro.\n")
              continue
      except ValueError:
          print("Valor inválido. O número deve ser um inteiro.\n")
          continue

      if num_int <= 0:
          print("Valor inválido. O número deve ser maior que zero.\n")
          continue

      fib1, fib2 = 0, 1
      while fib2 < num_int:
          fib1, fib2 = fib2, fib1 + fib2

      if fib2 == num_int:
          print(num_int, "pertence à sequência de Fibonacci\n")
      else:
          print(num_int, "não pertence à sequência de Fibonacci\n")
