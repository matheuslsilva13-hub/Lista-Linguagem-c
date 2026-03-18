#include <stdio.h>
#include <stdlib.h>

//avisar o compilador que existem estas funções
void exercicio27();
void exercicio28();


int main()
{
    int opcao;
    do{
        //Exibição do menu
        printf("\n\n---MENU PRINCIPAL---\n");
        printf("27 - Calculo da Diferença entre Dois Números Inteiros\n");
        printf("28 - Classificação de Número Positivo ou Negativo\n");
        printf("29 - Cálculo da Média e Verificação de Aprovação\n");
        printf("30 - Cálculo da Média e Verificação de Aprovação com Exame\n");
        printf("31 - Resolução de Equação de Segundo Grau\n");
        printf("32 - Ordenação de Três Números Inteiros\n");
        printf("33 - Valores Divisíveis por 2 e 3\n");
        printf("34 -  Valores Divisíveis por 2 ou 3\n");
        printf("35 -  Maior e Menor Valor\n");
        printf("36 - Par ou Ímpar\n");
        printf("37 - Verificação de Faixa de Valor\n");
        printf("38 - Verificação de Valor Menor ou Igual a 3\n");
        printf("39 - Múltiplo de 3 e 5\n");
        printf("40 - Soma e Verificação\n");
        printf("41 - Multiplicação e Verificação\n");
        //continua...

        //leitura da opcao desejada
        printf("Digite a opcao desejada ");
        scanf("%d",&opcao);

        switch (opcao){
        case 27:
            exercicio27(); //chama a função exercicio27
            break;
        case 28:
            exercicio28();
            break;
        case 29:
            exercicio29();
            break;
        case 30:
            exercicio30();
            break;
        case 31:
            exercicio31();
            break;
        case 32:
            exercicio32();
            break;
        case 33:
            exercicio33();
            break;
        case 34:
            exercicio34();
            break;
        case 35:
            exercicio35();
            break;
        case 36:
            exercicio36();
            break;
        case 37:
            exercicio37();
            break;
        case 38:
            exercicio38();
            break;
        case 39:
            exercicio39();
            break;
        case 40:
            exercicio40();
            break;
        case 41:
            exercicio41();
            break;
            //continua...

        default:
            printf("Opcao invalida! Tente novamente.\n");
        }
    } while (opcao != 0); //repetir até digitar o zero
    return 0;

}
//implementação das funções
void exercicio27(){
    int num1, num2, diferenca;
    printf("\n======Cálculo da Diferença entre Dois Números Inteiros======\n");

    // 1. Entrada de dados
    printf("Insira dois valores numericos:\n");
    scanf("%d", &num1);
    scanf("%d", &num2);
 // 2. Processamento de dados
    if (num1 > num2) {
        diferenca = num1 - num2;
        // 3. Saida de dados
        printf("O resultado da diferenca entre %.1d e %.1d e igual a %.1d\n", num1, num2, diferenca);
    }
    else if (num2 > num1) {
        diferenca = num2 - num1;
        // Saida de dados
        printf("O resultado da diferenca entre %.1d e %.1d e igual a %.1d\n", num2, num1, diferenca);
    }
    else {
        diferenca = num1 - num2;
        // Saida de dados
        printf("Os numeros sao iguais. A diferenca entre %.1d e %.1d e igual a %.1d\n", num1, num2, diferenca);
    }
}
void exercicio28(){
    int num1;
    printf("======Classificação de Número Positivo ou Negativo======");
    //1 Entrada de dados
    printf( "\ninsira um valor numerico\n");
    scanf("%d",&num1);
    //2 Processamentos de dados
    if (num1 >= 1) {
        printf("\n%.1d (Esse numero e positivo)",num1);
    }
    else if(num1 < 0){
        printf("%.1d (Esse numero e negativo)",num1);
    }
    else{
        printf("%.1d (Esse numero e neutro)",num1);
    }
}
void exercicio29()
{
    float n1,n2,n3,n4,media;
    printf("======Cálculo da Média e Verificação de Aprovação======");
    //1.Entrada de dados
    printf("\nInsira os valores de suas quatro notas\n");
    scanf("%f",&n1);
    scanf("%f",&n2);
    scanf("%f",&n3);
    scanf("%f",&n4);
    //2. processamento de dados
    media = (n1 + n2 + n3 + n4) / 4;
    //3.saida de dado
    if (media >=5){
        printf("\n %.1f (Aprovado)",media);
    }
    else if (media < 5)
        printf("\n %.1f (Reprovado)",media);
}
void exercicio30()
{
   float nota1, nota2, nota3, nota4, media, exame, nova_media;

    printf("\n======Calculo da Media e Verificacao de Aprovacao======\n");

    // 1. Entrada de Dados
    printf("Insira os valores das quatro notas bimestrais (separadas por espaco ou enter):\n");
    scanf("%f", &nota1);
    scanf("%f", &nota2);
    scanf("%f", &nota3);
    scanf("%f", &nota4);

    // 2. Processamento de dados
    media = (nota1 + nota2 + nota3 + nota4) / 4;

    // 3. Verificacao e Saida de Dados
    if (media >= 7.0) {
        printf("\nMedia: %.1f | Situacao: Aprovado\n", media);
    }
    else if (media >= 5.0) {

        printf("\nMedia: %.1f | Situacao: Exame\n", media);


        printf("Insira a nota do exame: ");
        scanf("%f", &exame);


        nova_media = (media + exame) / 2;


        if (nova_media > 5.0) {
            printf("Nova Media: %.1f | Situacao: Aprovado em Exame\n", nova_media);
        } else {
            printf("Nova Media: %.1f | Situacao: Reprovado\n", nova_media);
        }
    }
    else {
        // Se a média inicial for menor que 5, reprova direto
        printf("\nMedia: %.1f | Situacao: Reprovado\n", media);
    }
}
void exercicio31()
{
     float a,b,c,x1,x2,d;
    printf("======Resolução de Equação de Segundo Grau======");
    //1.ENtrada de dadod
    printf("\nInsira os valores dos coeficientes a , b e c\n");
    scanf("%f",&a);
    scanf("%f",&b);
    scanf("%f",&c);
    //Processamento de dados
    d =pow(b, 2) - 4 * a * c;
    if(d >= 0 ){
        x1 =(-b + sqrt(d))/ pow(a, 2);
        x2 =(-b - sqrt(d))/ pow(a, 2);
        //Saida de dados
        printf("\n x1 = %.1f | x2 = %.1f \n",x1,x2);
    }
}
void exercicio32()
{
     int n1,n2,n3;
     printf("======Ordenação de Três Números Inteiros======");
     //1. entrada de dados
     printf("\nInsira o valor dos tres numericos\n");
     scanf("%d",&n1);
     scanf("%d",&n2);
     scanf("%d",&n3);
     //2. Processamento de dados
  if (n1 <= n2 && n2 <= n3) {
        printf("\nOrdem crescente: %d | %d | %d\n", n1, n2, n3);
    }
    else if (n1 <= n3 && n3 <= n2) {
        printf("\nOrdem crescente: %d | %d | %d\n", n1, n3, n2);
    }
    else if (n2 <= n1 && n1 <= n3) {
        printf("\nOrdem crescente: %d | %d | %d\n", n2, n1, n3);
    }
    else if (n2 <= n3 && n3 <= n1) {
        printf("\nOrdem crescente: %d | %d | %d\n", n2, n3, n1);
    }
    else if (n3 <= n1 && n1 <= n2) {
        printf("\nOrdem crescente: %d | %d | %d\n", n3, n1, n2);
    }
    else {

        printf("\nOrdem crescente: %d | %d | %d\n", n3, n2, n1);
}
}
void exercicio33()
{
    int a,b,c,d;
    printf("======Valores Divisíveis por 2 e 3======");
    //entrada de dados
    printf("\nInsira quatro valores numericos\n");
    scanf("%d",&a);
    scanf("%d",&b);
    scanf("%d",&c);
    scanf("%d",&d);
    //processamento de dados
   if (a % 2 == 0 && a % 3 == 0 && b % 2 == 0 && b % 3 == 0 && c % 2 == 0 && c % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d | %d | %d\n", a, b, c, d);
    }

    else if (a % 2 == 0 && a % 3 == 0 && b % 2 == 0 && b % 3 == 0 && c % 2 == 0 && c % 3 == 0) {
        printf("\n%d | %d | %d\n", a, b, c);
    }
    else if (a % 2 == 0 && a % 3 == 0 && b % 2 == 0 && b % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d | %d\n", a, b, d);
    }
    else if (a % 2 == 0 && a % 3 == 0 && c % 2 == 0 && c % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d | %d\n", a, c, d);
    }
    else if (b % 2 == 0 && b % 3 == 0 && c % 2 == 0 && c % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d | %d\n", b, c, d);
    }

    else if (a % 2 == 0 && a % 3 == 0 && b % 2 == 0 && b % 3 == 0) {
        printf("\n%d | %d\n", a, b);
    }
    else if (a % 2 == 0 && a % 3 == 0 && c % 2 == 0 && c % 3 == 0) {
        printf("\n%d | %d\n", a, c);
    }
    else if (a % 2 == 0 && a % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d\n", a, d);
    }
    else if (b % 2 == 0 && b % 3 == 0 && c % 2 == 0 && c % 3 == 0) {
        printf("\n%d | %d\n", b, c);
    }
    else if (b % 2 == 0 && b % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d\n", b, d);
    }
    else if (c % 2 == 0 && c % 3 == 0 && d % 2 == 0 && d % 3 == 0) {
        printf("\n%d | %d\n", c, d);
    }
    // Casos isolados: E se SÓ UM numero for divisivel?
    else if (a % 2 == 0 && a % 3 == 0) {
        printf("\n%d\n", a);
    }
    else if (b % 2 == 0 && b % 3 == 0) {
        printf("\n%d\n", b);
    }
    else if (c % 2 == 0 && c % 3 == 0) {
        printf("\n%d\n", c);
    }
    else if (d % 2 == 0 && d % 3 == 0) {
        printf("\n%d\n", d);
    }

else if (a % 3 == 0 && a % 2 == 0){
    printf("\n%d",a);
}
else if (b % 3 == 0 && b % 2 == 0){
    printf("\n%d",b);
}
else if (c % 3 == 0 && c % 2 == 0){
    printf("\n%d",c);
}
else if (d % 3 == 0 && d % 2 == 0){
    printf("\n%d",d);
}
}
void exercicio34() {
    int a, b, c, d;
    printf("\n====== Valores Divisiveis por 2 ou 3 ======\n");

    // 1. Entrada de dados
    printf("Insira quatro valores inteiros:\n");
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    scanf("%d", &d);

    // 2. Processamento e Saida
    printf("Valores encontrados: ");
    if (a % 2 == 0 || a % 3 == 0) {
        printf("%d | ", a);
    }
    if (b % 2 == 0 || b % 3 == 0) {
        printf("%d | ", b);
    }
    if (c % 2 == 0 || c % 3 == 0) {
        printf("%d | ", c);
    }
    if (d % 2 == 0 || d % 3 == 0) {
        printf("%d | ", d);
    }
    printf("\n");
}

void exercicio35() {
    int a, b, c, d, e, maior, menor;
    printf("\n====== Maior e Menor Valor ======\n");

    // 1. Entrada de dados
    printf("Insira 5 valores numericos inteiros:\n");
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);
    scanf("%d", &d);
    scanf("%d", &e);

    // 2. Processamento (Assumimos que o primeiro é o maior e o menor, e testamos o resto)
    maior = a;
    menor = a;

    if (b > maior) maior = b;
    if (b < menor) menor = b;

    if (c > maior) maior = c;
    if (c < menor) menor = c;

    if (d > maior) maior = d;
    if (d < menor) menor = d;

    if (e > maior) maior = e;
    if (e < menor) menor = e;

    // 3. Saida
    printf("Maior valor: %d | Menor valor: %d\n", maior, menor);
}

void exercicio36() {
    int a;
    printf("\n====== Par ou Impar ======\n");

    // 1. Entrada de dados
    printf("Insira um valor inteiro:\n");
    scanf("%d", &a);

    // 2. Processamento e Saida
    if (a % 2 == 0) {
        printf("O numero %d e Par\n", a);
    } else {
        printf("O numero %d e Impar\n", a);
    }
}

void exercicio37() {
    int valor;
    printf("\n====== Verificacao de Faixa de Valor ======\n");

    // 1. Entrada de dados
    printf("Insira um numero entre 1 e 9:\n");
    scanf("%d", &valor);

    // 2. Processamento e Saida
    if (valor >= 1 && valor <= 9) {
        printf("O valor %d esta na faixa permitida.\n", valor);
    } else {
        printf("O valor %d NAO esta na faixa permitida.\n", valor);
    }
}

void exercicio38() {
    int a;
    printf("\n====== Verificacao de Valor Menor ou Igual a 3 ======\n");

    // 1. Entrada de dados
    printf("Insira um valor inteiro:\n");
    scanf("%d", &a);

    // 2. Processamento e Saida
    if (a <= 3) {
        printf("Resultado: %d\n", a);
    }
}

void exercicio39() {
    int a;
    printf("\n====== Multiplo de 3 e 5 ======\n");

    // 1. Entrada de dados
    printf("Insira um numero inteiro:\n");
    scanf("%d", &a);

    // 2. Processamento e Saida
    if (a % 3 == 0 && a % 5 == 0) {
        printf("O numero %d e multiplo de 3 e 5 ao mesmo tempo!\n", a);
    }
}

void exercicio40() {
    int a, b, c, s;
    printf("\n====== Soma e Verificacao ======\n");

    // 1. Entrada de dados
    printf("Insira tres valores numericos:\n");
    scanf("%d", &a);
    scanf("%d", &b);
    scanf("%d", &c);

    // 2. Processamento
    s = a + b + c;

    // 3. Saida condicionada
    if (s > 100) {
        printf("A soma e maior que 100. Resultado: %d\n", s);
    }
}

void exercicio41() {
    int a, m;
    printf("\n====== Multiplicacao e Verificacao ======\n");

    // 1. Entrada de dados
    printf("Insira um numero inteiro:\n");
    scanf("%d", &a);

    // 2. Processamento
    m = a * 2;

    // 3. Saida condicionada
    if (m > 30) {
        printf("O resultado da multiplicacao e maior que 30. Resultado: %d\n", m);
    }
}
