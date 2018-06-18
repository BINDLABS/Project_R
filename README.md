# Project_R

1. Initialize - (com.bindlabs.projectr.main.MainAPI)
```java
public MainAPI(Context c){}
```
Example : 
```java
MainAPI api = new MainAPI(MainActivity.this);
```


2. 본인 보유 총 금액 (원화)
```java
public Map<String, String> getTotalWon(){}
```
Example : 
```java
String amount = api.getTotalWon().get("won");
```


3. 본인 보유 코인 및 금액
```java
public ArrayList\<Coin\> getAllCoin(){}
```
Example : 
```java
ArrayList\<Coin\> coins = api.getAllCoin();

    public class Coin {
        public String type;
        public String coin;
        public String won;
    }
```

