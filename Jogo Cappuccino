#include <stdio.h>
#include <locale.h>
#include <time.h>
#include <conio.h>
#include <windows.h>
#include <stdlib.h>

struct tabuleiro{
int altura;
int jogador;};

typedef struct{
int cor;
int contpecas;
int soma;
} jogador;

void textcolor(int cor){
    static int __BACKGROUND;
    HANDLE h = GetStdHandle ( STD_OUTPUT_HANDLE );
    CONSOLE_SCREEN_BUFFER_INFO csbiInfo;
    GetConsoleScreenBufferInfo(h, &csbiInfo);
    SetConsoleTextAttribute(GetStdHandle (STD_OUTPUT_HANDLE),cor + (__BACKGROUND << 4));}

void limpatela(){
    system("cls");}

void voltar(){
    printf("\n\nPressione qualquer tecla para voltar ao menu  ");
    getch();
    limpatela();}

int main(){
    setlocale(LC_ALL, "");
int opcmenu=1, opcjogar, casa, i;

while(opcmenu !=4){
    limpatela();
    printf(" ----------------------------- JOGO CAPPUCCINO ----------------------------- ");
    printf("\n\n 1 - Jogar ");
    printf("\n 2 - Regras ");
    printf("\n 3 - Créditos ");
    printf("\n 4 - Sair ");
    printf("\n\n Opção: ");
    scanf("%d",&opcmenu);
switch(opcmenu){
case 1: {
    limpatela();
    while(opcjogar!=999){
        printf(" ----------------------------- JOGO CAPPUCCINO ----------------------------- ");
        printf("\n\n 1 - Nova Partida");
        printf("\n 2 - Carregar Partida");
        printf("\n 3 - Replay");
        printf("\n 4 - Voltar ao menu");
        printf("\n\nOpção: ");
        scanf("%d", &opcjogar);
        if(opcjogar==1){
            int fim=1;
            while(fim != 999){
            limpatela();
            textcolor(15);

int i, j, aleatorio;
int cont[4]={5,5,5,5};
srand((unsigned)time(NULL));
struct tabuleiro matriz[5][5];

for(i=0; i<5 ;i++){
    for(j=0; j<5 ; j++){
        if((i==0&&j==0)||(i==0&&j==4)||(i==2&&j==2)||(i==4&&j==0)||(i==4&&j==4)){
        matriz[i][j].altura=0;}
        else{
        matriz[i][j].altura=1;}}}

//deixando o tabuleiro aleatorio
for(i=0; i<5 ;i++){
    for(j=0; j<5 ; j++){
        if((i==0&&j==0)||(i==0&&j==4)||(i==2&&j==2)||(i==4&&j==0)||(i==4&&j==4)){
                matriz[i][j].jogador=9;}
        else{
        aleatorio=(rand()%4);
        while(cont[aleatorio]==0){
        aleatorio=(rand()%4);}
        matriz[i][j].jogador=aleatorio;
        cont[aleatorio]--;}}}


char peca[3];
int movimento;
int li, co,turno=0, partida=1,p;

//inicio do loop da partida
do{

int jogando=4, aux[4];
aux[0]=0;
aux[1]=0;
aux[2]=0;
aux[3]=0;

//verifica se ainda existem jogadores com jogadas válidas
    for(p=0; p<4; p++){
      for(i=0; i<5; i++){
        for(j=0; j<5; j++){
        if(matriz[i][j].jogador==p){
            if((matriz[i-1][j].altura>0)&&(matriz[i-1][j].altura<=matriz[i][j].altura)){
                if((i-1<0)||(j<0)||(i-1>4)||(j>4)){ }
                else{aux[p]++;}}
            if((matriz[i-1][j+1].altura>0)&&(matriz[i-1][j+1].altura<=matriz[i][j].altura)){
                if((i-1<0)||(j+1<0)||(i-1>4)||(j+1>4)){ }
                else{aux[p]++;}}
            if((matriz[i][j-1].altura>0)&&(matriz[i][j-1].altura<=matriz[i][j].altura)){
                if((i<0)||(j-1<0)||(i>4)||(j-1>4)){ }
                else{aux[p]++;}}
            if((matriz[i][j+1].altura>0)&&(matriz[i][j+1].altura<=matriz[i][j].altura)){
                if((i<0)||(j+1<0)||(i>4)||(j+1>4)){ }
                else{aux[p]++;}}
            if((matriz[i+1][j-1].altura>0)&&(matriz[i+1][j-1].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j-1<0)||(i+1>4)||(j-1>4)){ }
                else{aux[p]++;}}
            if((matriz[i+1][j].altura>0)&&(matriz[i+1][j].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j<0)||(i+1>4)||(j>4)){ }
                else{aux[p]++;}}
            if((matriz[i+1][j+1].altura>0)&&(matriz[i+1][j+1].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j+1<0)||(i+1>4)||(j+1>4)){ }
                else{aux[p]++;}}  }   }   }
                    if(aux[p]==0){
                    jogando--;}}

//se não tiver mais jogadas válidas a partida encerra
if(jogando==0){
partida--;}

else{
 int validaturno=0;
 //verifica se o jogador tem peça válida
 //se não tiver, vai pular o turno dele
     for(i=0; i<5; i++){
        for(j=0; j<5; j++){
        if(matriz[i][j].jogador==turno){
            if((matriz[i-1][j].altura>0)&&(matriz[i-1][j].altura<=matriz[i][j].altura)){
                if((i-1<0)||(j<0)||(i-1>4)||(j>4)){ }
                else{validaturno++;}}
            if((matriz[i-1][j+1].altura>0)&&(matriz[i-1][j+1].altura<=matriz[i][j].altura)){
                if((i-1<0)||(j+1<0)||(i-1>4)||(j+1>4)){ }
                else{validaturno++;}}
            if((matriz[i][j-1].altura>0)&&(matriz[i][j-1].altura<=matriz[i][j].altura)){
                if((i<0)||(j-1<0)||(i>4)||(j-1>4)){ }
                else{validaturno++;}}
            if((matriz[i][j+1].altura>0)&&(matriz[i][j+1].altura<=matriz[i][j].altura)){
                if((i<0)||(j+1<0)||(i>4)||(j+1>4)){ }
                else{validaturno++;}}
            if((matriz[i+1][j-1].altura>0)&&(matriz[i+1][j-1].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j-1<0)||(i+1>4)||(j-1>4)){ }
                else{validaturno++;}}
            if((matriz[i+1][j].altura>0)&&(matriz[i+1][j].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j<0)||(i+1>4)||(j>4)){ }
                else{validaturno++;}}
            if((matriz[i+1][j+1].altura>0)&&(matriz[i+1][j+1].altura<=matriz[i][j].altura)){
                if((i+1<0)||(j+1<0)||(i+1>4)||(j+1>4)){ }
                else{validaturno++;}}  }   }       }

if(validaturno>0){
    int conta=0;
//imprime o tabuleiro na tela
limpatela();
textcolor(15);
printf("    1    2    3    4    5");
for(i=0; i<5 ;i++){
        textcolor(15);
        printf("\n %c", 97+i);
    for(j=0; j<5 ; j++){
textcolor(matriz[i][j].jogador+1);
if(matriz[i][j].jogador==9){
    textcolor(15);}
printf("| %d |", matriz[i][j].altura);}
}

int mo1,mo2,mo3,mo4,mo6,mo7,mo8,mo9;
do{
textcolor(turno+1);

printf("\nTurno do jogador: %d", turno+1);
printf("\nEscolha a peça: ");
scanf("%s", &peca);
li=peca[0]-97;
co=peca[1]-49;

textcolor(15);

if((matriz[li-1][co-1].altura>0)&&(matriz[li-1][co-1].altura<=matriz[li][co].altura)){
        if((li-1<0)||(co-1<0)||(li-1>4)||(co-1>4)){ }
        else{
    conta++;
    mo7=1;}}
if((matriz[li-1][co].altura>0)&&(matriz[li-1][co].altura<=matriz[li][co].altura)){
        if((li-1<0)||(co<0)||(li-1>4)||(co>4)){ }
        else{
    conta++;
    mo8=1;}}
if((matriz[li-1][co+1].altura>0)&&(matriz[li-1][co+1].altura<=matriz[li][co].altura)){
        if((li-1<0)||(co+1<0)||(li-1>4)||(co+1>4)){ }
        else{
    conta++;
    mo9=1;;}}
if((matriz[li][co-1].altura>0)&&(matriz[li][co-1].altura<=matriz[li][co].altura)){
        if((li<0)||(co-1<0)||(li>4)||(co-1>4)){ }
        else{
    conta++;
    mo4=1;}}
if((matriz[li][co+1].altura>0)&&(matriz[li][co+1].altura<=matriz[li][co].altura)){
        if((li<0)||(co+1<0)||(li>4)||(co+1>4)){ }
        else{
    conta++;
    mo6=1;}}
if((matriz[li+1][co-1].altura>0)&&(matriz[li+1][co-1].altura<=matriz[li][co].altura)){
        if((li+1<0)||(co-1<0)||(li+1>4)||(co-1>4)){ }
        else{
    conta++;
    mo1=1;}}
if((matriz[li+1][co].altura>0)&&(matriz[li+1][co].altura<=matriz[li][co].altura)){
        if((li+1<0)||(co<0)||(li+1>4)||(co>4)){ }
        else{
    conta++;
    mo2=1;}}
if((matriz[li+1][co+1].altura>0)&&(matriz[li+1][co+1].altura<=matriz[li][co].altura)){
    if((li+1<0)||(co+1<0)||(li+1>4)||(co+1>4)){ }
        else{
    conta++;
    mo3=1;}}
else if(conta<=0){
    printf("\nEscolha outra peça");}
}while((li>5)||(co>5)||(matriz[li][co].jogador!=turno)||(conta<=0));

printf("\nmovimentos possiveis: %d\n", conta);
textcolor(turno+1);
int jogada=0;

do{
textcolor(15);
printf("Movimento: ");
scanf("%d", &movimento);

//se digitar 7
   if(movimento==7 && mo7==1){
        if((matriz[li-1][co-1].altura>0)&&(matriz[li-1][co-1].altura<=matriz[li][co].altura)){
                if((li-1<0)||(co-1<0)||(li-1>4)||(co-1>4)){ }
                matriz[li][co].jogador = 9;
                matriz[li-1][co-1].altura = (matriz[li][co].altura) + (matriz[li-1][co-1].altura);
                matriz[li][co].altura = 0;
                matriz[li-1][co-1].jogador = turno;
                movimento=0;
                mo7=0;
                jogada=1;}}
 //se digitar 8
    else if(movimento==8 && mo8==1){
            if((matriz[li-1][co].altura>0)&&(matriz[li-1][co].altura<=matriz[li][co].altura)){
                    if((li-1<0)||(co<0)||(li-1>4)||(co>4)){ }
            matriz[li][co].jogador=9;
            matriz[li-1][co].altura= (matriz[li][co].altura) + (matriz[li-1][co].altura);
            matriz[li][co].altura=0;
            matriz[li-1][co].jogador=turno;
            movimento=0;
            mo8=0;
            jogada=1;}}
//se digitar 9
    else if(movimento==9 && mo9==1){
            if((matriz[li-1][co+1].altura>0)&&(matriz[li-1][co+1].altura<=matriz[li][co].altura)){
                    if((li-1<0)||(co+1<0)||(li-1>4)||(co+1>4)){ }
            matriz[li][co].jogador=9;
            matriz[li-1][co+1].altura= (matriz[li][co].altura) + (matriz[li-1][co+1].altura);
            matriz[li][co].altura=0;
            matriz[li-1][co+1].jogador=turno;
            mo9=0;
            movimento=0;
            jogada=1;}}
//se digitar 4
    else if(movimento==4 && mo4==1){
            if((matriz[li][co-1].altura>0)&&(matriz[li][co-1].altura<=matriz[li][co].altura)){
                    if((li<0)||(co-1<0)||(li>4)||(co-1>4)){ }
                matriz[li][co].jogador=9;
                matriz[li][co-1].altura= (matriz[li][co].altura) + (matriz[li][co-1].altura);
                matriz[li][co].altura=0;
                matriz[li][co-1].jogador=turno;
                mo4=0;
                movimento=0;
                jogada=1;}}
//se digitar 6
    else if(movimento==6 && mo6==1){
            if((matriz[li][co+1].altura>0)&&(matriz[li][co+1].altura<=matriz[li][co].altura)){
                    if((li<0)||(co+1<0)||(li>4)||(co+1>4)){ }
                matriz[li][co].jogador=9;
                matriz[li][co+1].altura= (matriz[li][co].altura) + (matriz[li][co+1].altura);
                matriz[li][co].altura=0;
                matriz[li][co+1].jogador=turno;
                mo6=0;
                movimento=0;
                jogada=1;}}
//se digitar 1
    else if(movimento==1 && mo1==1){
            if((matriz[li+1][co-1].altura>0)&&(matriz[li+1][co-1].altura<=matriz[li][co].altura)){
                    if((li+1<0)||(co-1<0)||(li+1>4)||(co-1>4)){ }
                matriz[li][co].jogador=9;
                matriz[li+1][co-1].altura= (matriz[li][co].altura) + (matriz[li+1][co-1].altura);
                matriz[li][co].altura=0;
                matriz[li+1][co-1].jogador=turno;
                mo1=0;
                movimento=0;
                jogada=1;}}
//se digitar 2
    else if(movimento==2 && mo2==1){
            if((matriz[li+1][co].altura>0)&&(matriz[li+1][co].altura<=matriz[li][co].altura)){
                    if((li+1<0)||(co<0)||(li+1>4)||(co>4)){ }
                matriz[li][co].jogador=9;
                matriz[li+1][co].altura= (matriz[li][co].altura) + (matriz[li+1][co].altura);
                matriz[li][co].altura=0;
                matriz[li+1][co].jogador=turno;
                mo2=0;
                movimento=0;
                jogada=1;}}
//se digitar 3
   else if(movimento==3 && mo3==1){
        if((matriz[li+1][co+1].altura>0)&&(matriz[li+1][co+1].altura<=matriz[li][co].altura)){
                if((li+1<0)||(co+1<0)||(li+1>4)||(co+1>4)){ }
                matriz[li][co].jogador=9;
                matriz[li+1][co+1].altura= (matriz[li][co].altura) + (matriz[li+1][co+1].altura);
                matriz[li][co].altura=0;
                matriz[li+1][co+1].jogador=turno;
                mo3=0;
                movimento=0;
                jogada=1;}}
    else{}
}while(jogada!=1);
}
}
if(turno<3){
    turno++;}
else{
    turno=0;}

}while(partida==1);
//fim do loop da partida

//resultado da partida
int pontos[4];
pontos[0]=0;
pontos[1]=0;
pontos[2]=0;
pontos[3]=0;
limpatela();
        for(p=0; p<5; p++){
            for(i=0; i<5; i++){
                for(j=0; j<5; j++){
                        if(matriz[i][j].jogador==p){
                            pontos[p]+=matriz[i][j].altura;}}}}
        printf(" ----------------------------- Pontuação Final----------------------------- ");
        for(i=0; i<4; i++){
            textcolor(i+1);
            printf("\n Jogador %d: %d", i+1, pontos[i]);}
            textcolor(15);

//vendo quem ganhou
    if((pontos[3]>=pontos[2])&&(pontos[3]>=pontos[1])&&(pontos[3]>=pontos[0])){
    textcolor(4);
    printf("\n\nJogador 4 ganhou");
    printf("\nPARABÉNS!!!!");}
    else if((pontos[2]>pontos[3])&&(pontos[2]>=pontos[1])&&(pontos[2]>=pontos[0])){
    textcolor(3);
    printf("\n\nJogador 3 ganhou");
    printf("\nPARABÉNS!!!!");}
    else if((pontos[1]>pontos[3])&&(pontos[1]>pontos[2])&&(pontos[1]>=pontos[0])){
    textcolor(2);
    printf("\n\nJogador 2 ganhou");
    printf("\nPARABÉNS!!!!");}
    else if((pontos[0]>pontos[3])&&(pontos[0]>pontos[2])&&(pontos[0]>pontos[1])){
    textcolor(1);
    printf("\n\nJogador 1 ganhou");
    printf("\nPARABÉNS!!!!");}

    textcolor(15);
            voltar();
            break;
            }}
        else if(opcjogar==2){
            limpatela();
            printf("Você escolheu carregar uma partida");
            printf("\nEm breve em atualizações futuras...");
            voltar();}
        else if(opcjogar==3){
            limpatela();
            printf("Você escolheu ver o replay da partida");
            printf("\nEm breve em atualizações futuras...");
            voltar();}
        else if(opcjogar==4)
            voltar();
    break;}
    break;}
case 2: {
    limpatela();
    printf(" ----------------------------- JOGO CAPPUCCINO ----------------------------- ");
    printf("\n\n ---------------------------------- Regras -------------------------------");
    printf("\n\n    - Cappuccino é um jogo abstrato para até quatro jogadores cujo\n      objetivo é ter a maior quantidade de pilhas sobre \n      seu domínio ao final da partida\n");
    printf("\n    - Só pode mover a peça para casas adjacentes");
    printf("\n    - Caso o espaço esteja vazio(zerado), não é possível realizar o movimento");
    printf("\n    - Caso o espaço tenha uma peça, ele só poderá se mover \n      se a peça tiver altura igual ou inferior à sua");
    printf("\n    - Em caso de empates, será uasada a ordem do turno inversa para desempatar\n\n");
    textcolor(1);
    printf("\n    - Jogador 1 = ");
    printf("AZUL");
    textcolor(2);
    printf("\n    - Jogador 2 = ");
    printf("VERDE");
    textcolor(3);
    printf("\n    - Jogador 3 = ");
    printf("CIANO");
    textcolor(4);
    printf("\n    - Jogador 4 = ");
    printf("VERMELHO");
    textcolor(15);

    voltar();
    break;}
case 3:{
    limpatela();
    printf(" ----------------------------- JOGO CAPPUCCINO ----------------------------- ");
    printf("\n\n------------------- Projeto de introdução à programação --------------------");
    printf("\n------------------------ Jogo Cappuccino Adaptado --------------------------");
    printf("\n\nDocente: Roberto Hugo Wanderley Pinheiro");
    printf("\nDiscente: Camila Vanessa de Matos Sousa");
    voltar();
    break;}
case 4:
    return 0;}}}
