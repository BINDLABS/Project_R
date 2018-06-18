# Project_R

## Initialize - (com.bindlabs.projectr.main.MainAPI)
```java
public MainAPI(Context c){}
```
Example : 
```java
MainAPI api = new MainAPI(MainActivity.this);
```
</br>

## 본인 보유 총 금액 (원화)
```java
public Map<String, String> getTotalWon(){}
```
Example : 
```java
String amount = api.getTotalWon().get("won");
```
</br>

## 본인 보유 코인 및 금액
```java
public ArrayList<Coin> getAllCoin(){}

public class Coin {
    public String type;
    public String coin;
    public String won;
}
```
Example : 
```java
ArrayList<Coin> coins = api.getAllCoin();
```
</br>

## 거래기록
```java
public ArrayList<Tx> getTransactions(String type){}

public class Tx {
    public String type;
    public String addr;
    public String amount;
    public long timestamp;
    public String diff;
}
```
Example : 
```java
ArrayList<Tx> transactions = api.getTransactions("xrp");
```
</br>

## 프로필 이름
```java
public String getProfileName(String addr){}
```
Example : 
```java
String name = api.getProfileName("");
```
</br>

## 총 결제 코인(리플)
```java
public double getXrpFinalCost(long won){}
```
Example : 
```java
double xrp = api.getXrpFinalCost(10000);
```
</br>

## 프로필 전체
```java
public Map<String, String> getProfile(String addr){}
```
Example : 
```java
Map<String, String> profile = api.getProfile("");
String name = profile.get("name");//프로필 이름
String pic = profile.get("pic");//프로필 이미지 주소
String detail = profile.get("detail");//프로필 내용
```
</br>

## ~~결제~~(추가작업 필요)
```java
public int confirmPayment(){}// 0:결제실패, 1:결제성공
```
Example : 
```java
api.confirmPayment();
```
</br>

## API키 설정(빗썸)
```java
public int setAPI(String apikey, String secretkey){}// 0:실패, 1:성공
```
Example : 
```java
api.setAPI("","");
```
</br>

## 프로필설정 - 전체
```java
public String setProfile(int uid,String lt,String name, Bitmap pic, String detail){}//결과
```
Example : 
```java
api.setProfile(0,loginToken,"이름",bitmap,"프로필설명");
```
</br>

## 프로필설정 - 이름
```java
public String setProfileName(int uid,String lt,String name){}//결과
```
Example : 
```java
api.setProfileName(0,loginToken,"이름");
```
</br>

## 프로필설정 - 사진
```java
public String setProfilePicture(int uid,String lt,Bitmap pic){}//결과
```
Example : 
```java
api.setProfilePicture(0,loginToken,bitmap);
```
</br>

## 프로필설정 - 설명
```java
public String setProfileDetail(int uid,String lt,String detail){}//결과
```
Example : 
```java
api.setProfileDetail(0,loginToken,"프로필설명");
```
