## Code for my final project:

    import java.util.Random;
      import java.awt.*;
      import java.awt.event.*;
      import javax.swing.*;

      public class FinalProject extends JFrame {
      private JLabel labelintro1, labelintro2, labelintro3, labelHigh, labelLow, labelWin;
      private JButton btnGuess;
      private JTextField txtEnterNum;
      private int intGuess, intRandomNumber;


      private Container c = getContentPane();

      public static void main(String[] args) {


        FinalProject fp = new FinalProject();
        fp.setSize(500,500);
        fp.setVisible(true);
        fp.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

      }

      public FinalProject() {
      c.setLayout(new FlowLayout(1,175,25));


      setTitle("Guess My Number!");

      labelintro1 = new JLabel("I have a number from 1 to 100!");
      add(labelintro1);
      labelintro2 = new JLabel("Can you guess my number?");
      add(labelintro2);
      labelintro3 = new JLabel(" Please enter your guess:");
      add(labelintro3);
      txtEnterNum = new JTextField(10);
      add(txtEnterNum);
      txtEnterNum.setToolTipText("Insert your number here.");

      btnGuess = new JButton("Guess Number");
      add(btnGuess);
      btnGuess.setToolTipText("Click here to guess your entered number.");
      labelHigh = new JLabel("Too High!");
      labelLow = new JLabel("Too Low!");
      labelWin = new JLabel("You Win!");

      Handler bhandler = new Handler();
      btnGuess.addActionListener(bhandler);

      Random randNum = new Random();
      intRandomNumber = randNum.nextInt(100) + 1;
      System.out.print(intRandomNumber);

      add(labelWin);
      add(labelLow);
      add(labelHigh);
      labelWin.setVisible(false);
      labelLow.setVisible(false);
      labelHigh.setVisible(false);

      }

      public class Handler implements ActionListener {

      public void actionPerformed(ActionEvent ev) {

      String strGuess = txtEnterNum.getText();
      intGuess = Integer.parseInt(strGuess);

      if(intGuess == intRandomNumber) {
          getContentPane().setBackground(Color.green);

          labelWin.setVisible(true);
          labelLow.setVisible(false);
          labelHigh.setVisible(false);

        }

      if(intGuess < intRandomNumber) {
          getContentPane().setBackground(Color.red);
          labelLow.setVisible(true);
          labelWin.setVisible(false);
          labelHigh.setVisible(false);
        }

      if (intGuess > intRandomNumber) {
          getContentPane().setBackground(Color.blue);
          labelHigh.setVisible(true);
          labelWin.setVisible(false);
          labelLow.setVisible(false);
        }

      }
      }
      }

