# super_trunfo.c

#include <stdio.h>

struct Carta {
    char estado;
    char codigo[4];
    char nomeCidade[50];
    int populacao;
    float area;
    float pib;
    int pontosTuristicos;
};

void limparBuffer() {
    int c;
    while ((c = getchar()) != '\n' && c != EOF);
}

int main() {
    struct Carta carta1, carta2;

    printf("Cadastro da Carta 1:\n");

    printf("Estado (A-H): ");
    scanf(" %c", &carta1.estado);
    limparBuffer();

    printf("Código (ex: A01): ");
    scanf("%3s", carta1.codigo);
    limparBuffer();

    printf("Nome da Cidade: ");
    fgets(carta1.nomeCidade, sizeof(carta1.nomeCidade), stdin);

    printf("População: ");
    scanf("%d", &carta1.populacao);

    printf("Área (km²): ");
    scanf("%f", &carta1.area);

    printf("PIB (em bilhões): ");
    scanf("%f", &carta1.pib);

    printf("Nº de Pontos Turísticos: ");
    scanf("%d", &carta1.pontosTuristicos);
    limparBuffer();

    printf("\nCadastro da Carta 2:\n");

    printf("Estado: ");
    scanf(" %c", &carta2.estado);
    limparBuffer();

    printf("Código (ex: B02): ");
    scanf("%3s", carta2.codigo);
    limparBuffer();

    printf("Nome da Cidade: ");
    fgets(carta2.nomeCidade, sizeof(carta2.nomeCidade), stdin);

    printf("População: ");
    scanf("%d", &carta2.populacao);

    printf("Área (km²): ");
    scanf("%f", &carta2.area);

    printf("PIB (em bilhões): ");
    scanf("%f", &carta2.pib);

    printf("Nº de Pontos Turísticos: ");
    scanf("%d", &carta2.pontosTuristicos);

    printf("\n----------------------\n");
    printf("Carta 1:\n");
    printf("Estado: %c\n", carta1.estado);
    printf("Código: %s\n", carta1.codigo);
    printf("Cidade: %s", carta1.nomeCidade);
    printf("População: %d\n", carta1.populacao);
    printf("Área: %.2f km²\n", carta1.area);
    printf("PIB: %.2f bilhões de reais\n", carta1.pib);
    printf("Pontos Turísticos: %d\n", carta1.pontosTuristicos);

    printf("\nCarta 2:\n");
    printf("Estado: %c\n", carta2.estado);
    printf("Código: %s\n", carta2.codigo);
    printf("Cidade: %s", carta2.nomeCidade);
    printf("População: %d\n", carta2.populacao);
    printf("Área: %.2f km²\n", carta2.area);
    printf("PIB: %.2f bilhões de reais\n", carta2.pib);
    printf("Pontos Turísticos: %d\n", carta2.pontosTuristicos);

    return 0;
}
