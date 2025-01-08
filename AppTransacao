// Declarando uma lista encadeada ( no caso um nó )
typedef struct Transacao {
    float valor;
    char local[50];
    struct Transacao *next;
    
} Transacao;

void adicionarTransacao (Transacao **lista, float valor, const char *local) {
    Transacao *novaTransacao = (Transacao * ) malloc(sizeof(Transacao));
    novaTransacao->valor = valor;
    strcpy(novaTransacao->local, local);
    novaTransacao->next = NULL;
    
    if (*lista == NULL) {
        *lista = novaTransacao;
    } else {
        Transacao *temp = *lista;
        while(temp->next != NULL) {
            temp = temp->next;
        }
        temp->next = novaTransacao;
    }
}

void exibirTransacoes(Transacao *lista) {
    if (lista == NULL) {
        printf("Nenhuma transação registrada.\n");
        return;
    }
    Transacao *temp = lista;
    while (temp != NULL) {
        printf("Valor: %.2f | Local: %s\n", temp->valor, temp->local);
        temp = temp->next;
    }
}

int main() {
    Transacao *lista = NULL;  // Inicializa a lista vazia

    // Adicionando transações
    adicionarTransacao(&lista, 50.75, "Supermercado");
    adicionarTransacao(&lista, 20.30, "Transporte");
    adicionarTransacao(&lista, 100.00, "Restaurante");

    // Exibindo as transações
    printf("Transações registradas:\n");
    exibirTransacoes(lista);


    return 0;
}
