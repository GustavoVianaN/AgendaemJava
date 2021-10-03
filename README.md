/* criando agenda em java, vou fazer em inglês, para treinar */

/* In this project I will create a schedule in java with menu, registration people, and cellphone */

package structure;

public class schedule {

  public static void main(String[] args) {


/* I will declared a vetor with the data */

    String[] name = new String[20];

    String[] adress = new String[20];

    String[] telephone = new String[20];

    for (int i = 0; i < 20; i++)  {
      name[i] = "";
      telephone[i] = "";
      adress[i] = "";
    }
    
    String option = "";
    String continuar = "";
    int position = 0;
    String nameDelete = "";

    /* Declare the prohibited variable */

    Scanner prohibited = new Scanner(System.in);

    /* System.in in java means to take input from the keyboard or user. System. out in java means to print the output to console. */

    /* in the link if option outside equale a get out, if you has false, if the link in option outside equale a true, if you has true */

    do {

          System.out.printLn("Chosen the option: include - liste - delet - get out");  

          /* switch case improvement the performance */

          switch (option) {
            case "include":
              do {
                  System.out.print("Type the name: ");
                  name[position] = prohibited.nextLine();

                  System.out.print("Type the adress: ");
                  adress[position] = prohibited.nextLine();

                  System.out.print("Type the telephone: ");
                  telephone[position] = prohibited.nextLine();

                  //* solicited if the usuary wish registration other contact */

                  System.out.print("Wish continue the registration?");
                  coninuar = prohibited.nextline();

                  position++;


              } while (continuar.equals("Yes"));
              break;

            case "Liste":

              for (int i = 0; i < 20; i++) {

                if(!name[i].equals("")) { 

                System.out.println("Name: " + name[i] + "" + "Telephone" + telephone[i] + " " + "Adress: " + adress[i]);
              }}

              break;
            
            case "Delete":

            System.out.println("who wish delete? ");
            delete = prohibited.nextLine();
            
            for (int i = 0; i < 20; i++) { 
              if(name[i].equals(nameDelete)) {
                
                name[i] = "";
                telephone[i] = "";
                adress[i] = "";
              }
            }


              break;
            
            case "get out":
              System.out.println("Finished program");
              /* return in java do the method terminate */

              return;

            default:
              /* implement the situation */
              System.out.println("Invalid Option! Tye again!");
              break;
          }

    } while (!option.equals("go out"));

  }}
