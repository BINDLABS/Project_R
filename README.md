# Project_R

1. Initialize - (com.bindlabs.projectr.main.MainAPI)<br>
<code>public MainAPI(Context c){}</code><br>Example : <code>MainAPI api = new MainAPI(MainActivity.this);</code>

2. 본인 보유 총 금액 (원화)<br>
<code>public Map<String, String> getTotalWon(){}</code><br>Example : <code>String amount = api.getTotalWon().get("won");<br></code>

3. 본인 보유 코인 및 금액<br>
<code>public ArrayList<Coin> getAllCoin(){}</code><br>Example : <code>ArrayList<Coin> coins = api.getAllCoin();<br></code>
<br>Coin -<br>
<code>public class Coin {
    public String type;
    public String coin;
    public String won;
  }</code><br>
<br>
4. 거래기록<br>
<code></code>

5. 프로필 이름<br>
<code></code>

6. 총 결제 코인<br>
<code></code>

7. 프로필 전체<br>
<code></code>

8. 결제<br>
<code></code>

9. API키 설정<br>
<code></code>

10. 프로필설정 - 전체<br>
<code></code>

11. 프로필설정 - 이름<br>
<code></code>

12. 프로필설정 - 사진<br>
<code></code>

13. 프로필설정 - 설명<br>
<code></code>

14. QR코드 카메라<br>
<code></code>

15. QR코드 갤러리<br>
<code></code>

16. 푸쉬알림설정<br>
<code></code>

17. QR코드생성<br>
<code></code>

18. 회원가입<br>
<code></code>

19. 로그인<br>
<code></code>

20. 지갑주소확인<br>
<code></code>
