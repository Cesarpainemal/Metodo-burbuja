# Metodo-burbuja 
 // al momento de ingresarlo se me desordena, pero lo edito me muestra todo en orden.
 public static void main(String[] args) {
       
       Scanner intro = new Scanner(System.in);
        int x;
        int aux;
        System.out.println("Ingresar cantidad de numeros");
        x = intro.nextInt();
        int num[] = new int[x];
        for (int i = 0; i < num.length; i++) {
            num[i] = (int) (Math.random() * 20 + 1);
        }int consultas=0; 
        for (int i = 0; i < num.length; i++) {
            for (int j = 0; j < num.length; j++) {
                if (num[i] > num[j]) {
                    aux = num[i];
                    num[i] = num[j];
                    num[j] = aux;
                }
                consultas++;
                
            }
        }
        for (int i =0; i < num.length; i++) {
            System.out.print(num[i] + ", ");
        }
        System.out.print("la cant de consultas fueron "+consultas);
        
    

 }
