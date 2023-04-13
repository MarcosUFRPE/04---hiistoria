# 04---hiistoria

import java.util.Scanner;

public class Capitulo {
  
  Caracteristicapersonagem personagem;
  int novaenergia;
  String  nome;
  String texto;
  String[] escolhas;
  Scanner his;




        Capitulo( Caracteristicapersonagem personagem,
                   int novaenergia,
                   String  nome,
                  String texto,
                  String[] escolhas,
                  Scanner his
                   )
           {

            this.personagem=personagem;
            this.novaenergia=novaenergia;
            this.nome=nome;            
            this.texto=texto;
            this.escolhas=escolhas;          
            this.his=his;
        }


            
            /**
             * 
             */
             void mostra(){
              
              System.out.println(this.nome);
              System.out.println("________________________________");
              System.out.println(this.texto); 
              this.personagem.qtenergia(this.novaenergia);

           if (this.escolhas!=null){
               for(String escolha : escolhas){

                   System.out.println(escolha);
                  }

          
              

            }
              System.out.println("________________________________");
              
            }
 
            int escolher(){

              int nescolha=0;

              if (escolhas!=null){
               
                
                while(nescolha==0){
                String resp= his.nextLine();
                for (int n = 0; n < escolhas.length; n++) {
                 
                  if ( resp.equals(escolhas[n])){ 
                     nescolha=n;
                }
              }

              }
           
              }
             return nescolha;
            }

           }

 _______________________________________________________________________________
 // PARTE DA HISTORIA INTERATIVA
 ________________________________________________________________________________
 
 
 import java.util.Scanner;


/**
 * App
 */
public class App {

    /**
    * @param args
    */
   public static void main(String[] args) {
      
      
           
        
      Caracteristicapersonagem martin =new Caracteristicapersonagem();
      martin.nome="martin";
      martin.energia=100;
      martin.qtenergia(0);
   Caracteristicapersonagemassasino =new Caracteristicapersonagem();
    assasino.nome="assasino"; 
    assasino.energia=100;
    assasino.qtenergia(0);
   Caracteristicapersonagem joana =new Caracteristicapersonagem();
     joana.nome="Joana";   
     joana.energia=100;
     joana.qtenergia(0);  
    Caracteristicapersonagem espiritochefe=new Caracteristicapersonagem();
      espiritochefe.nome="joao";
      espiritochefe.altura=3.00f;
      espiritochefe.idade=500;
      espiritochefe.energia=300;
      espiritochefe.qtenergia(0);
   








      


         
          
          Scanner his=new Scanner(System.in);
         Capitulo capitulo1=new Capitulo( martin,
            0,
            "A  TRILHA PELA FLORESTA", 
           " Um certo dia três amigos,"+martin.nome+","assasino.nome+" e "+joana.nome+ ",resoveram fazer uma trilha pela floresta"
           +" "+"chegando lá  eles avistaram uma  casa abandonada. " +
           "O que eles tem que fazer?",
          new String[]{" ir até a casa"," passar direto "},
          
          his
           
         );

         
          capitulo1.mostra();
          int escolha=capitulo1.escolher();

         
         
         
         
         
         
         
         if (escolha==0){ 

            Capitulo capitulo3=new Capitulo( martin,
               0,
               "A CHEGADA A  CASA ABANDONADA", 
               " Chegando na casa abandonada ,eles entram e encontram um livro chamado ,os 7 espirito amaldiçoado . " +
               " o que eles tem que fazer? ",
                new String[] {" eles pegam o livro e ler "," deixam o livro queto "},
                 his
             
              );

            capitulo3.mostra();
             escolha=capitulo3.escolher();
            
            


           if (escolha==0){
            
            Capitulo capitulo4=new Capituloassasino,
               -10,
               "O ENCONTRO COM O ESPIRITO ", 
            "E assim que eles acabaram de ler o livro ,sete espito amaldiçoado despertam para atormentar a vida daqueles " +
            "que acordaram eles de seu sono profundo e entre esses sete espito está o " + espiritochefe.nome +
            " um espirito de "+" "+ espiritochefe.altura + "m de altura e " + espiritochefe.idade + " anos  de idade " +
            "e que quando era um homem foi um psicopata que matou milhares de pessoas "+
            "e que  quando a polic1ia pegou ele  torturou e matou ele nessa casa abandonada   e até " +
            "hoje seu espito vive nessa casa,sendo o lider dos outros seis espirito  ." + 

            "Agora a missão dos três amigos é encontrar uma forma de fazer com que os 7 espiro voltem "+
            " para o seu sono profundo,caso não  "+
            " os espirito vão pegar  atormenta e tortura eles ate morre. "+
            "sedo  que as portas da casa abandonada se fecharam quando os espiritos depestaram  "+  
            "assim os tres amigos nao tem como simplemente sair da casa . "  +
            "como eles nao conseguia sair da casa resolveram caçar alguma soluação dentro da casa " +
            " em busca de alguma solução eles acabam dando de cara com um dos espitos que acaba atacando eles " +
            "e que acaba acertado ,"assasino.nome+  " , com uma paulada  fazendo com quer " assasino.nome  +
            " perca  energia "
            
           , null,           
            his
             
              );
            capitulo4.mostra();
            
           } else if(escolha==1) {

            Capitulo capitulo5=new Capitulo(martin,
               0,
               "O LIVRAMENTO",
               "E deixando o livro quieto eles se livra do tormento dos 7 espiritos amaldiçoados." ,
               null,                
               his
               );
            
            capitulo5.mostra();
           
           }
           }else if(escolha==1) { 

             Capitulo capitulo2=new Capitulo(martin,
               0,
               "DIA NORMAL",
               "  E assim foi mais um dia normal na vida deles!",
               null, 
               his
               
                );
             
                capitulo2.mostra();


             
           }
       his.close();
         
    }

   }
}

   

