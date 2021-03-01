## Fala Devs :vulcan_salute: 
## Matriz Transposta - Java  :man_technologist:
### A transposta de uma matriz A é uma matriz que apresenta os mesmos elementos de A, só que colocados em uma posição diferente. Ela é obtida transportando-se ordenadamente os elementos das linhas de A para as colunas da transposta.  

[![Linkedin Badge](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white&link=https://www.w3schools.com/java/default.asp)](https://www.w3schools.com/java/default.asp)

```
public class MatrizTransposta {
		
	//ENTRADA DE DADOS MATRIZ
	static int [][] criaMatriz(int n, int m){
		int [][] matriz  = new int[n][m];
		
		//Gerando númeors aleatórios
		Random gerador = new Random();
		
		//Preenchendo os índices  
		for(int i = 0; i <matriz.length; i++) {
			for(int j = 0; j < matriz[0].length; j++) {
				matriz[i][i] = gerador.nextInt(100);
			}
		}
		return matriz;
	}
	
	//TRANSPOSTA
	static int [][] transposta(int [][] matriz){
		int [][] matrizTransposta = new int [matriz[0].length][matriz.length];		
		for(int i = 0; i < matrizTransposta.length; i++) {
			for(int j = 0; j < matrizTransposta[0].length; j++) {
				matrizTransposta[i][j] = matriz[j][i];
			}
		}
		
		return matrizTransposta;
	}
	
	//SAIDA DE DADOS
	static void imprimeMatriz(int [][] matriz) {
		for(int i = 0; i < matriz.length; i++) {
			for(int j = 0; j < matriz[i].length; j++) {
				System.out.print(matriz[i][j] + "\t");
			}
			System.out.print("\n");
		}
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int [][] matriz = criaMatriz(3,4);
		imprimeMatriz(matriz);
		System.out.println();
		System.out.println("=====TRANSPOSTA=====\n");
	
		int [][] transposta = transposta(matriz);
		imprimeMatriz(transposta);
	}
}

```
