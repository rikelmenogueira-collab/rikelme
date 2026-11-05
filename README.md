```python
print("=== Calculadora de Média Escolar ===")

nome = input("Digite o nome do aluno: ")

try:
    nota1 = float(input("Digite a primeira nota (0 a 10): "))
    nota2 = float(input("Digite a segunda nota (0 a 10): "))
    nota3 = float(input("Digite a terceira nota (0 a 10): "))

    if not all(0 <= nota <= 10 for nota in (nota1, nota2, nota3)):
        print("Erro: as notas devem estar entre 0 e 10.")
    else:
        media = (nota1 + nota2 + nota3) / 3

        print(f"\nAluno: {nome}")
        print(f"Média: {media:.2f}")

        if media >= 7:
            print("Situação: Aprovado")
        elif media >= 5:
            print("Situação: Recuperação")
        else:
            print("Situação: Reprovado")

except ValueError:
    print("Erro: digite as notas usando números.")
```
