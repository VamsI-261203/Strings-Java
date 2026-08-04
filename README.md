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
