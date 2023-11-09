# 44-project-pp
import java.util.Random;
import java.util.Scanner;
public class game2 {
public static void main(String[] args){
    int user;
    int computer,user_score=0,computer_score= 0;
    Random ob1  = new Random();
    int up_limit=3;
    int lw_limit=1;

    Scanner ob2 =new Scanner(System.in);
    int i=1;
    while(i<4){
        System.out.println("****************");
        System.out.println("chosse > Rock, paper, scisser");
        System.out.println("enter 1 for rock");
        System.out.println("enter 2 for paper");
        System.out.println("enter 3 for scisser");

        user = ob2.nextInt();
        switch(user){
            case 1->System.out.println("you select Rock");
            case 2->System.out.println("you select paper");
            case 3->System.out.println("you select scisser ");
        }
        computer = ob1.nextInt( up_limit)+lw_limit;
        switch(computer){
            case 1->System.out.println("computer select Rock");
            case 2->System.out.println("computer select paper");
            case 3->System.out.println("computer select scisser ");}


        if(user ==1&&computer==1||user==2&&computer==2||user==3&&computer==3){
            System.out.print("tie");

        }else if(user==1&&computer==2){
            System.out.println("you lose");
            user_score+=0;
            computer_score+=1;
        }else if(user==2&&computer==1){
            System.out.println("you win");
            user_score+=1;
            computer_score+=0;
        }else if(user==1&&computer==3){
            System.out.println("you win");
            user_score+=1;
            computer_score+=0;
        }else if(user==3&&computer==1){
            System.out.println("you lose");
            user_score+=0;
            computer_score+=1;
        }else if(user==2&&computer==3){
            System.out.println("you lose");
            user_score+=0;
            computer_score+=1;
        }else if (user==3&&computer==2){
            System.out.println("you win");
            user_score+=1;
            computer_score+=0;
        }
        ++i;
      
        
    }
    {if(user_score < computer_score){
        System.out.print("you lose");
       // System.out.println(user_score);
        //System.out.println(computer_score);
    }else {
        System.out.print("you win");
        //System.out.println(user_score);
        //System.out.println(computer_score);
    }
    System.out.println("thankyou for playing");

    }
}
    
}
