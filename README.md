# Structs.cpp
#include <iostream>
#include <string>
using namespace std;

// Definindo a estrutura para representar bandas de música
struct Banda {
    string nome;        // Nome da banda
    string tipoMusica;  // Tipo de música que a banda toca
    int numeroIntegrantes; // Número de integrantes
    int posicaoRanking; // Posição no ranking das 5 bandas favoritas
};

int main() {
    // Criando um array de 5 bandas
    Banda bandas[5];

    // Entrada dos dados das 5 bandas
    for (int i = 0; i < 5; i++) {
        cout << "Informe os dados da banda #" << i + 1 << ":" << endl;

        cout << "Nome da banda: ";
        getline(cin, bandas[i].nome); // Leitura do nome da banda

        cout << "Tipo de musica: ";
        getline(cin, bandas[i].tipoMusica); // Leitura do tipo de música

        cout << "Numero de integrantes: ";
        cin >> bandas[i].numeroIntegrantes; // Leitura do número de integrantes

        cout << "Posicao no ranking (1 a 5): ";
        cin >> bandas[i].posicaoRanking; // Leitura da posição no ranking

        cin.ignore(); // Ignora o newline residual após leitura de int
        cout << endl;
    }

    // Exibindo os dados das bandas
    cout << "Informacoes das bandas favoritas:" << endl;
    for (int i = 0; i < 5; i++) {
        cout << "Banda #" << i + 1 << ": " << endl;
        cout << "Nome: " << bandas[i].nome << endl;
        cout << "Tipo de Musica: " << bandas[i].tipoMusica << endl;
        cout << "Numero de Integrantes: " << bandas[i].numeroIntegrantes << endl;
        cout << "Posicao no Ranking: " << bandas[i].posicaoRanking << endl;
        cout << endl; 
    }
return 0;
}
