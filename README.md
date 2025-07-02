import javax.swing.*; import java.io.*;
public class LoginForm {
  public static void main(String[] a) throws Exception {
    String u = JOptionPane.showInputDialog("Username");
    String p = JOptionPane.showInputDialog("Password");
    String r = (String) JOptionPane.showInputDialog(null, "Role", "Select Role", 
      JOptionPane.QUESTION_MESSAGE, null, new String[]{"Patient", "Doctor"}, "Patient");
    try (BufferedReader br = new BufferedReader(new FileReader(r + ".txt"))) {
      String l; boolean f = false;
      while ((l = br.readLine()) != null) if (l.equals(u + "," + p)) f = true;
      JOptionPane.showMessageDialog(null, f ? "Login Success" : "Invalid Credentials");
    }
  }
}
