# Estrutura-em-C

#include <stdio.h>
#include <stdlib.h>
#include <Windows.h>
#include <locale.h>


void cadastro_notas() {
	system("cls");
	printf("Cadastro de Notas/Alunos\n");
	// agora vou digitar os dados de notas e alunos.
	
	
	
	system("pause");	
	return;
}
void alteracao_notas() {
	system("cls");
	printf("Alteração de Notas/Alunos\n");
	// agora vou alterar os dados de notas e alunos.
	
	
	
	system("pause");	
	return;
}

int main() {	
	setlocale(LC_ALL,"");
	int opcao=0;
	printf("Carregando o sistema... aguarde");
	Sleep(500);

	while ((opcao != 1) && (opcao !=2) && (opcao != 3)) {		
		// opcoes do menu
		system("cls");
		printf("Bem vindo ao meu sistema\n\n");
		printf("Menu\n");
		printf("----\n");
		printf("1-Cadastro de Notas/Alunos\n");
		printf("2-Alteracao de Notas/Alunos\n");
		printf("3-Sair\n");
		printf("Opção: ");
		scanf("%i",&opcao);
		// verificando as opcoes
		if (opcao == 1) {
			cadastro_notas();
			for (int contador = 0; contador < 5; contador ++){
			
			char nome_aluno[100]; 
			printf("\nEscreva o nome do aluno: \n ");
			scanf("%s", nome_aluno);			
			float nota1; 
			float nota2;
			float nota3;
			float nota4;
		
			printf("Escreva as notas dos alunos (número arredondado): \n ");
			scanf("%f" ,&nota1);
			scanf("%f" ,&nota2);	
			scanf("%f" ,&nota3);
			scanf("%f" ,&nota4);
			
			float nota = (nota1 + nota2 + nota3 + nota4);
		    float media = (nota/4);
		    
		    printf("A nota desse aluno é:\n", media);
		    
		    if (media < 4){
		    	printf("ALUNO REPROVADO \n");
			}else if (media < 6 && media > 4){
				printf("ALUNO APROVADO \n");
			}else {
				printf("ALUNO DE RECUPERAÇÃO \n");
			}
			opcao = 0;
		}
		} else {
			if (opcao == 2) {
				alteracao_notas();
				
				opcao = 0;
			} else {
				if (opcao == 3) {
					exit;
				}
			}
		}
	}
	
	return 0;
}
