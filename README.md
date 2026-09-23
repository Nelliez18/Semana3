Módulo calculadora.py
```python
# Em python
import calculadora
import ultilidades
print("--- TESTE CALCULADORA ---")
print(f"Somar 10 + 5: {calculadora.somar(10, 5)}")
print(f"Dividir 10 / 2: {calculadora.dividir(10, 2)}")
print(f"Dividir 10 / 0: {calculadora.dividir(10, 0)} (Tratado com sucesso!)")

print("\n--- TESTE UTILIDADES ---")
print(f"25°C para Fahrenheit: {ultilidades.celsius_para_fahrenheit(25)}°F")
print(f"Senha '123' é válida? {ultilidades.validar_senha('123')}")
print(f"Senha '123456' é válida? {ultilidades.validar_senha('123456')}")

# Testando Caixa com *precos
total_compras = ultilidades.caixa_com_precos(19.90, 5.50, 100.00, 4.25)
print(f"Total do Caixa (*precos): R$ {total_compras:.2f}")

# Testando Ficha do Aluno com **dados
print(ultilidades.ficha_aluno(nome="Maria", idade=21, curso="Medicina", matricula="2026MED"))

# Testando Lista Segura (Cópia Defensiva)
lista_orig = ["Maçã", "Banana"]
nova_list = ultilidades.lista_segura(lista_orig, "Laranja")
print(f"Lista Original (Intacta): {lista_orig}")
print(f"Nova Lista (Modificada): {nova_list}")
```
```portugol
// SEÇÃO: FUNÇÕES DA CALCULADORA

funcao real somar(real a, real b) {
    retorne a + b
}

funcao real subtrair(real a, real b) {
    retorne a - b
}

funcao real multiplicar(real a, real b) {
    retorne a * b
}

funcao real dividir(real a, real b) {
    se (b == 0.0) {
        // Como Portugol não possui 'None', retornamos um valor padrão de erro absurdo
        retorne -99999.0 
    } senao {
        retorne a / b
    }
}
```
Módulo utilidades.py
