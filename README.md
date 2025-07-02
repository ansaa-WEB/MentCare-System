import javax.swing.*;
import java.awt.*;
import java.io.*;

public class MHSM {
    public static void main(String[] args) {
        JFrame f = new JFrame("MHS"); f.setSize(500, 300); f.setDefaultCloseOperation(3);
        JPanel p = new JPanel(); p.setLayout(null); f.add(p);
        String[] roles = {"Login", "Register"}; int y = 50;
        for (String r : roles) { JButton b = new JButton(r); b.setBounds(180, y, 120, 40); y += 60; p.add(b); }
        f.setLocationRelativeTo(null); f.setVisible(true);
    }
}
