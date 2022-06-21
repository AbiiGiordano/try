# try
class Arbol : public grafo{
    
private:
public:
    Arbol();
    //Arbol::Arbol() : Grafo(){}
    
    //Esecifico el método de Grafo, para que solo agregue si no se forma ciclo
    //DEBO ADAPTAR LA IMPLEMENTACION PARA USAR EL OBJETO ARISTA!!! VERIFICAR BORDES :(
    agregar_camino(Arista arista);
    
    
};


class Arbol_expansion{
    
private:
    Arbol arbol;
    int** matriz_adyacencia;
    Lista<Vértice<Lectura*>> vertices;
    cola_prioridad DE STL;
    
public:
    // NO SE SI ESTOS TRES VAN ACA O EN LA CLASE GRAFO
    obtener_aristas(); // Recorre la matriz y va viendo las aristas existentes en el grafo
    /*
    void Arbol_expansion::obtener_aristas(){
        for(int i = 0; i < vertices->obtener_cantidad_elementos(); i++){
            for (int j = 0; j < vertices->obtener_cantidad_elementos(); j++){
                int peso = matriz_adyacencia[i][j];
                if (peso != INFINITO){
                    Arista nueva_arista = new Arista(i, j, peso);
                    AGREGO LA NUEVA ARISTA A LA COLA DE PRIORIDAD;
                }
            }
        }
    }
    */
    
    crear_arbol_expansion(Arbol arbol_expansioon);
    /*
    void Arbol_expansion:.crear_arbol_expansion(Arbol arbol_expansion){
        while (cola_prioridad no este vacia){
            arista_actual = cola_prioridad.desencolar();
            // SI NO LO DEVUELVE, VEO EL TOPE Y DESENCOLO
            arbol_expansion.agregar_camino(arista_actual)   //!!!!
        }
    }
    
    */
    
    

    Arbol_expansion(int** matriz_adyacencia, Lista<Vértice<Lectura*>> vertices);  // Crea un 
    /*
    Arbol_expansion::Arbol_expansion(matriz_adyacencia, vertices){
        this->matriz_adyacencia = matriz_adyacencia;
        this->vertices = vertices;
        cola_prioridad = ¿STL?;
        
        arbol_expansion = new Arbol();// SUBCLASE DE GRAFO, EN DONDE AGREGAR_CAMINO DEBE VERIFICAR QUE NO SE CREEN CICLOS
        crear_arbol_expansion(arbol_expansion);
    }
    
    */
    
    
    
};

