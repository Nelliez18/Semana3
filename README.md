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
// Em portugol
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
    if (b == 0.0) {
        return -99999.0  // Retorna None sem quebrar a execução do programa
    }
    retorne a / b
}
```
Módulo utilidades.py
```python
# Em python
# SEÇÃO: FUNÇÕES DE UTILIDADES

def celsius_para_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def validar_senha(senha):
    return len(senha) >= 6

def caixa_com_precos(*precos):
    total = sum(precos)
    return total

def ficha_aluno(**dados):
    ficha = "--- Ficha do Aluno ---\n"
    for chave, valor in dados.items():
        ficha += f"{chave.capitalize()}: {valor}\n"
    return ficha

def lista_segura(lista_original, item):
    # Cópia defensiva: gera uma nova lista sem alterar a referência original
    nova_lista = lista_original.copy()
    nova_lista.append(item)
    return nova_lista
```
```portugol
// Em portugol
// SEÇÃO: FUNÇÕES DE UTILIDADES

funcao real celsius_para_fahrenheit(real celsius) {
    retorne (celsius * 9.0 / 5.0) + 32.0
}

funcao logico validar_senha(cadeia senha) {
    retorne txt.numero_caracteres(senha) >= 6
}

funcao real caixa_com_precos(real precos[], inteiro tamanho) {
    real total = 0.0
    para (inteiro i = 0; i < tamanho; i++) {
        total = total + precos[i]
    }
    retorne total
}

funcao ficha_aluno(cadeia nome, inteiro idade, cadeia curso, cadeia matricula) {
    escreva("--- Ficha do Aluno ---\n")
    escreva("Nome: ", nome, "\n")
    escreva("Idade: ", idade, "\n")
    escreva("Curso: ", curso, "\n")
    escreva("Matricula: ", matricula, "\n")
}

funcao lista_segura(cadeia lista_original[], inteiro tamanho_origem, cadeia destino[], cadeia item) {
    // Cópia defensiva: gera uma nova lista sem alterar a referência original
    para (inteiro i = 0; i < tamanho_origem; i++) {
        destino[i] = lista_original[i]
    }
    destino[tamanho_origem] = item
}
```
Script Principal
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
// Em portugol
programa {
    // Importando as bibliotecas do projeto e a biblioteca de Texto nativa
    inclua biblioteca calculadora
    inclua biblioteca utilidades
    inclua biblioteca Texto --> txt

    funcao inicio() {
        print("--- TESTE CALCULADORA ---")
        print("Somar 10 + 5: " + calculadora.somar(10.0, 5.0))
        print("Dividir 10 / 2: " + calculadora.dividir(10.0, 2.0))
        
        real res_div = calculadora.dividir(10.0, 0.0)
        se (res_div == -99999.0) {
            print("Dividir 10 / 0: Erro (Tratado com sucesso!)")
        } senao {
            print("Dividir 10 / 0: " + res_div)
        }

        print("\n--- TESTE UTILIDADES ---")
        print("25°C para Fahrenheit: " + utilidades.celsius_para_fahrenheit(25.0) + "°F")
        print("Senha '123' é válida? " + utilidades.validar_senha("123"))
        print("Senha '123456' é válida? " + utilidades.validar_senha("123456"))

        // Testando Caixa com *precos
        real lista_precos[] = {19.90, 5.50, 100.00, 4.25}
        real total_compras = utilidades.caixa_com_precos(lista_precos, 4)
        print("Total do Caixa (*precos): R$ " + total_compras)

        // Testando Ficha do Aluno com **dados
        utilidades.ficha_aluno("Maria", 21, "Medicina", "2026MED")

        // Testando Lista Segura (Cópia Defensiva)
        cadeia lista_orig[] = {"Maçã", "Banana", ""}
        cadeia nova_list[3]
        
        utilidades.lista_segura(lista_orig, 2, nova_list, "Laranja")
        print("Lista Original (Intacta): [" + lista_orig[0] + ", " + lista_orig[1] + "]")
        print("Nova Lista (Modificada): [" + nova_list[0] + ", " + nova_list[1] + ", " + nova_list[2] + "]")
    }

    // Função auxiliar apenas para simular o comando print() do Python com quebra de linha
    funcao print(cadeia texto) {
        escreva(texto, "\n")
    }
}
```
