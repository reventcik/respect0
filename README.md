```java
package bank;

import java.util.Scanner;
import database.getmoney;

public class bank() {

private String email;

  public void oldBank(Bank bank) {
    Scanner scanner = new Scanner(System.in);
    Thread.sleep(1000);
    try {
      System.out.println("Email gir"); 
      email = scanner.next();
      Database db = new Database(email);
      System.out.println("Paranız : " + Integer.valueOf(db.getmoney));
    } catch (SQLException e) {
      System.out.println(e.getMessage());
      System.out.println(e.getErrorCode());
    } finally {
      db.close();
    }
  }
}
```
