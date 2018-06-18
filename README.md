# Project_R

1. Initialize - (com.bindlabs.projectr.main.MainAPI)
============
public MainAPI(Context c){}
Example : 
MainAPI api = new MainAPI(MainActivity.this);



2. 본인 보유 총 금액 (원화)
============
public Map<String, String> getTotalWon(){}

Example : 
String amount = api.getTotalWon().get("won");



3. 본인 보유 코인 및 금액
============
public ArrayList\<Coin\> getAllCoin(){}

Example : 
ArrayList\<Coin\> coins = api.getAllCoin();

    public class Coin {
        public String type;
        public String coin;
        public String won;
    }

