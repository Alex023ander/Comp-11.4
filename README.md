# Comp-11.4

import java.util.Scanner;
public class Comp114 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String input="";
        String[] file={"U","C","P"};
        String[] name={"Unclassified","Confidental","Proprietary"};
        InvalidDocumentCodeException e= new InvalidDocumentCodeException("Invalid");
        System.out.println("Input U,C,P(DONE to end)");
        input=scan.nextLine();
        while(!input.equals("DONE")){
            try{
                for(int i=0;i<3;i++){
                    if(input.equals(file[i])){
                        System.out.println(name[i]);
                        break;
                    }
                    if(i==2){
                        throw e;
                    }
                    
                }
            }
            catch(InvalidDocumentCodeException ex){
                System.out.println("Invalid"); 
            }
            System.out.println("Input U,C,P(DONE to end)");
            input=scan.nextLine();
        }
        System.out.println("Method ended");
    }
    
}
