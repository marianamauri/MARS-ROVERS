package sondaposicao;
public class Sonda {
    public static final Integer N = 1;
    public static final Integer E = 2;
    public static final Integer S = 3;
    public static final Integer O = 4;
    Integer x = 0;
    Integer y = 0;
    Integer lado = N;
    public Sonda() {
    }
    public void setPosicao(Integer x, Integer y, Integer facing) {
        this.x = x;
        this.y = y;
        this.lado = lado;
    }
    public void printPosicao() {
        char dir = 'N';
        if (lado == 1){
            dir = 'N'; } 

      else if (lado == 2) {
            dir = 'E'; } 

     else if (lado == 3) {
            dir = 'S'; } 

    else if (lado == 4) {
            dir = 'O'; }

        System.out.println(x   " "   y   " "   dir);
    }

    public void process(String commands) {
        for (int idx = 0; idx < commands.length(); idx  ) {
            process(commands.charAt(idx));
        }
    }
    private void process(Character command) {
        if (command.equals('L')) {
            turnLeft();
        } else if (command.equals('R')) {
            turnRight();
        } else if (command.equals('M')) {
            move();
        } else {
            throw new IllegalArgumentException(
                    "Tente novamente.");
        }
    }
    private void movimento() {
        if (lado == N) {
            this.y  ;
        } else if (lado == E) {
            this.x  ;
        } else if (lado == S) {
            this.y--;
        } else if (lado == W) {
            this.x--;
        }
    }
    private void virarEsquerda() {
        lado = (lado - 1) < N ? W : lado - 1;
    }
    private void virarDireita() {
        facing = (lado   1) > W ? N : lado  1;
    }
