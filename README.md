# Buy-and-sell-Stock-java-
class buyandsell{
    public static void main(String[] args){
        int prices[]={7,1,2,6,3};
        int buy_price=prices[0];
        int max_profit=0;
        int current_profit=0;
        for(int i=0;i<prices.length;i++){
            if(prices[i]<buy_price){
                buy_price=prices[i];
            }
            else{
                current_profit=prices[i]-buy_price;
                max_profit=Math.max(max_profit,current_profit);
            }
        }
        System.out.println(max_profit);
    }
}

import java.util.*;
class validparanthesis{
    public static void main(String[] args){
        String s="{[({})]}";
        Stack<Character> st=new Stack<>();
        for(int i=0;i<s.length();i++){
            char ch=s.charAt(i);
            if(ch=='('){
                st.push(')');
            }
            else if(ch=='{'){
                st.push('}');
            }
            else if(ch=='['){
                st.push(']');
            }
            else if( st.isEmpty() || st.pop()!=ch ){
                System.out.println("Not valid");
            }
        }
        if(st.isEmpty()){
            System.out.println("Valid String Paranthesis");
        }
        else{
            System.out.println("Not Valid");
        }
    }
}
