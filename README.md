import java.awt.*;
import java.util.*;

public class Hal {
  public static void main(String[] args) throws Exception {
    Robot hal = new Robot();
    Random random = new Random();
    while(true) {
      try {
        Thread.sleep(Double.valueOf(1000*60*4.9).longValue());
      } catch(InterruptedException ite) {
          ite.printStackTrace();
      }
      int x = random.nextInt() % 640;
      int y = random.nextInt() % 480;
      hal.mouseMove(x, y);
    }
  }
}
