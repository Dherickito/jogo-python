import random

def jogo_da_forca():
    print("🎯 Bem-vindo ao Jogo da Forca!")
    print("Tente adivinhar a palavra antes de acabar suas chances!")

    palavras = ["python", "computador", "programador", "teclado", "internet", "desenvolvimento", "algoritmo"]

    palavra_secreta = random.choice(palavras).lower()
    letras_descobertas = ["_"] * len(palavra_secreta)
    letras_erradas = []
    tentativas = 6  

    while tentativas > 0 and "_" in letras_descobertas:
        print("\nPalavra:", " ".join(letras_descobertas))
        print("Letras erradas:", ", ".join(letras_erradas))
        print(f"Tentativas restantes: {tentativas}")

        letra = input("Digite uma letra: ").lower()

        if len(letra) != 1 or not letra.isalpha():
            print("❗ Digite apenas uma letra válida.")
            continue
        if letra in letras_erradas or letra in letras_descobertas:
            print("⚠️ Você já tentou essa letra.")
            continue

        if letra in palavra_secreta:
            for i, l in enumerate(palavra_secreta):
                if l == letra:
                    letras_descobertas[i] = letra
            print("✅ Boa! A letra está na palavra.")
        else:
            letras_erradas.append(letra)
            tentativas -= 1
            print("❌ A letra não está na palavra.")

    if "_" not in letras_descobertas:
        print(f"\n🎉 Parabéns! Você acertou a palavra: {palavra_secreta.upper()}")
    else:
        print(f"\n💀 Fim de jogo! A palavra era: {palavra_secreta.upper()}")

if __name__ == "__main__":
    jogo_da_forca()
