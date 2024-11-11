import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class Main {

    public static void main(String[] args) {

       JFrame frame = new JFrame("clicker game");
       JLabel showCLicks = new JLabel("0");
       JButton clickButton = new JButton("+");
       JButton decButton = new JButton("-");
       JButton resetButton = new JButton("reset");


       frame.setLayout(new GridLayout(3,1));
       frame.setSize(300,300);
       frame.add(showCLicks);
       frame.add(clickButton);
       frame.add(decButton);
       frame.add(resetButton);

       frame.setVisible(true);

       clickButton.addActionListener(new ActionListener(){

           public void actionPerformed(ActionEvent e){
               int counter = Integer.parseInt(showCLicks.getText());
               counter++;
               showCLicks.setText(String.valueOf(counter));
           }
       });
              decButton.addActionListener(new ActionListener(){

           public void actionPerformed(ActionEvent e){
               int counter = Integer.parseInt(showCLicks.getText());
               counter--;
               showCLicks.setText(String.valueOf(counter));
           }
       });
        resetButton.addActionListener(new ActionListener(){

            public void actionPerformed(ActionEvent e){
                showCLicks.setText("0");
            }
        });

    }
}
