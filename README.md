# Project_R V_1.0

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
ArrayList<Tx> transactions = api.getTransactions("all");//all week month
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
int result = api.confirmPayment();
```
</br>

## API키 설정(빗썸)
```java
public int setAPI(String apikey, String secretkey){}// 0:실패, 1:성공
```
Example : 
```java
int result = api.setAPI("","");
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
</br>

## ~~QR코드 스캔~~(추가작업 필요)
</br>

## 사진에서 QR코드 인식
```java
public void scanImage(Bitmap qr){};
```
Example : 
```java
api.scanImage(QRbitmap);
```
</br>

## ~~푸쉬알림설정~~(추가작업 필요)
```java
public int setNotificationAt(String type, double price){}// 0:실패, 1:성공
```
Example : 
```java
int result = api.setNotificationAt("xrp",1000);
```
</br>

## QR코드 생성
```java
public Bitmap getQR(String type, long won, int size){}
```
Example : 
```java
Bitmap qrcode = api.getQR("xrp",10000,120);
```
</br>

## 회원가입
```java
public int register(String email,String pass,String r_code){}// 0:실패, 1:성공
```
Example : 
```java
int result = api.register("test@test.com","test password","recommender code");
```
</br>

## 로그인
```java
public Map<String, String> login(String email,String pass){}
```
Example : 
```java
Map<String, String> result = api.login("test@test.com","test password");
String loginToken = result.get("loginToken");
int uid = Integer.parseInt(result.get("uid"));
```
</br>

## 내 지갑주소
```java
public String getWallet(String type){}
```
Example : 
```java
String myWalletAddr = api.getWallet("xrp");
```
