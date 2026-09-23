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
´´´portugol
// SEÇÃO: SCRIPT PRINCIPAL (EXECUÇÃO DIRETA)
programa {
    // Inclui a biblioteca de Texto para ajudar na simulação do código
    inclua biblioteca Texto --> txt

    funcao inicio() {
        // --- TESTE CALCULADORA ---
        escreva("--- TESTE CALCULADORA ---\n")
        escreva("Somar 10 + 5: ", somar(10.0, 5.0), "\n")
        escreva("Dividir 10 / 2: ", dividir(10.0, 2.0), "\n")
        
        real res_div_zero = dividir(10.0, 0.0)
        se (res_div_zero == -99999.0) {
            escreva("Dividir 10 / 0: Erro detectado (Tratado com sucesso!)\n")
        } senao {
            escreva("Dividir 10 / 0: ", res_div_zero, "\n")
        }

        // --- TESTE UTILIDADES ---
        escreva("\n--- TESTE UTILIDADES ---\n")
        escreva("25°C para Fahrenheit: ", celsius_para_fahrenheit(25.0), "°F\n")
        escreva("Senha '123' é válida? ", validar_senha("123"), "\n")
        escreva("Senha '123456' é válida? ", validar_senha("123456"), "\n")

        // Testando Caixa com *precos (Simulado via Vetor)
        real lista_precos[4] = {19.90, 5.50, 100.00, 4.25}
        real total_compras = caixa_com_precos(lista_precos, 4)
        escreva("Total do Caixa (*precos): R$ ", total_compras, "\n")

        // Testando Ficha do Aluno com **dados (Simulado via chamada direta estruturada)
        ficha_aluno("Maria", 21, "Medicina", "2026MED")

        // Testando Lista Segura (Cópia Defensiva de Vetores)
        cadeia lista_orig[3] = {"Maçã", "Banana", ""}
        cadeia nova_list[3]
        
        lista_segura(lista_orig, 2, nova_list, "Laranja")
        
        escreva("Lista Original (Intacta): [", lista_orig[0], ", ", lista_orig[1], "]\n")
        escreva("Nova Lista (Modificada): [", nova_list[0], ", ", nova_list[1], ", ", nova_list[2], "]\n")
    }

    // Coloque as funções dos códigos 2 e 3 aqui embaixo para rodar tudo junto!
}
´´´

Módulo utilidades.py
