# FxTrading
package hii;

public class Trade {
	String name1;
    int amount;
    String rate1;
    String currencyPair1;

}public class Keerthi {
	static ArrayList<Trade> arr=new ArrayList<Trade>();
    static Double rateOfInterset_USDINR=66.00;

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		while(true){
	        Scanner s=new Scanner(System.in);
	        System.out.println(" l Book Trade -1\n l Print Trades - 2\n l Exit - 3");
	        int opt=s.nextInt();
	        if(opt==1){
	            Trade tem=new Trade();
	            System.out.println("Enter customer Name");
	            tem.name1=s.next();
	            s.nextLine();
	            System.out.println("Enter Currency Pair");
	            tem.currencyPair1=s.next();
	            if(!tem.currencyPair1.equals("USDINR")){
	                System.out.println("Invalid Input");
	            }
	            else{
	            System.out.println("Enter amount to transfer");
	            tem.amount=s.nextInt();
	            System.out.println("Do you want to get Rate");
	            tem.rate1=s.next();
	            s.nextLine();
	            // System.out.println();
	            System.out.println("You are transferring INR"+(tem.amount*rateOfInterset_USDINR)+"to "+tem.name1);
	            System.out.println("Book/Cancel this trade?");
	            String book_cancel=s.next();
	            if(book_cancel.equals("Book")){
	                arr.add(tem);
	                System.out.println("Trade for "+tem.currencyPair1+" has been booked with rate"+rateOfInterset_USDINR+",The amount of Rs"+(tem.amount*rateOfInterset_USDINR)+"will be transferred in 2 working days to "+tem.name1);
	            }
	            else{
	                System.out.println("Trade is Canceled.");
	            }
	        }
	        }
	        else if(opt==2){
	            System.out.println("TradeNo\tCurrencyPair\tCustomerName\tAmount\tRate");
	            for(int iter2=0;iter2<arr.size();iter2++){
	                Trade tem=arr.get(iter2);
	                System.out.println((iter2+1)+"\t\t"+tem.currencyPair1+"\t\t"+tem.currencyPair1+"\t\t"+(tem.amount*rateOfInterset_USDINR)+"\t\t"+rateOfInterset_USDINR);
	            }
	        }
	        else{
	            System.out.println("Do you really want to exit (y/n)");
	            char op=s.next().charAt(0);
	            if(op=='Y'){
	                System.out.println("Bye - have a good day");
	                break;
	            }
	        }
	    }

	}

}
