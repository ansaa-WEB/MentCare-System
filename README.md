import javax.swing.*; import java.io.*;
public class RegisterForm { 
  public static void main(String[] a) {
    String u = JOptionPane.showInputDialog("Enter Username");
    String p = JOptionPane.showInputDialog("Enter Password");
    String r = (String) JOptionPane.showInputDialog(null, "Role", "Select Role", 
      JOptionPane.QUESTION_MESSAGE, null, new String[]{"Patient", "Doctor"}, "Patient");
    try (BufferedWriter w = new BufferedWriter(new FileWriter(r + ".txt", true))) {
      w.write(u + "," + p); w.newLine();
      JOptionPane.showMessageDialog(null, "Registered as " + r);
    } catch (IOException e) { e.printStackTrace(); }
  }
}
