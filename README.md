package main;

import java.util.Scanner;

public class Main {

	 public static void main(String[] args) {
	      Scanner sc = new Scanner(System.in);
	      
	      
	      System.out.println("====가위바위보====");
	      System.out.println("1. 가위 2. 바위 3.보");
	      System.out.println("승리시 3점 패배시 -2점");
	      
	      String y = "";
	      int a = 0;
	      int b = 0;
	      int c = 0;
	      int score = 0;
	      
	      while(true){
	         int com = (int)(Math.random()*3+1);
	         String x = sc.nextLine();
	         switch(com) {
	         case 1 : y = "가위" ;
	               break;
	         case 2 : y = "바위";
	               break;
	         case 3 : y = "보" ;
	               break;
	         }
	      if(x.equals("가위")) {
	         if(y.equals("보")) {
	         System.out.println("승리");
	         System.out.println("컴퓨터 : " + y);
	         a = a + 1;
	         score = score+3;
	         }
	         else if(y.equals("바위")) {
	            System.out.println("패배");
	            System.out.println("컴퓨터 : " + y);
	            b = b + 1;
	            score = score -1;
	         }
	         else if(y.equals("가위")) {
	            System.out.println("무승부");
	         System.out.println("컴퓨터 : " + y);
	         c = c + 1;
	         }
	      }
	      else if(x.equals("바위")) {
	         if(y.equals("가위")) {
	            System.out.println("승리");
	            System.out.println("컴퓨터 : " + y);
	            a = a + 1;
	            score = score+3;
	            }
	            else if(y.equals("보")) {
	               System.out.println("패배");
	               System.out.println("컴퓨터 : " + y);
	               b = b + 1;
	               score = score -1;
	            }
	            else if(y.equals("바위")) {
	               System.out.println("무승부");
	            System.out.println("컴퓨터 : " + y);
	            c = c + 1;
	            }
	         }
	      else if(x.equals("보"))  {
	         if(y.equals("바위")) {
	            System.out.println("승리");
	            System.out.println("컴퓨터 : " + y);
	            a = a + 1;
	            score = score+3;
	            }
	            else if(y.equals("가위")) {
	               System.out.println("패배");
	               System.out.println("컴퓨터 : " + y);
	               b = b + 1;
	               score = score -1;
	            }
	            else if(y.equals("보")) {
	               System.out.println("무승부");
	            System.out.println("컴퓨터 : " + y);
	            c = c + 1;
	            }
	         
	      }
	      else if(x.equals("종료")) {
	         System.out.println("프로그램을 종료 합니다.");
	         System.out.println("승 : " + a + " 패 : " + b + " 무 : " + c);
	         System.out.println("점수: " + score);
	         break;
	      }
	      }
	      
	   }

	}
