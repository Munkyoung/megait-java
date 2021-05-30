# JFrame게임

```java
package com.day18.homework;

import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JOptionPane;

class NewFrame {
	JButton tmp = new JButton();

	JFrame frame;
	JButton[] Barr;
	int i = 0;

	public void PlayGame() {

		frame = new JFrame("Test");
		Barr = new JButton[16];

		for (int i = 0; i < Barr.length; i++) {
			Barr[i] = new JButton(String.valueOf(i + 1));
		}

		for (int i = 0; i < 20; i++) {
			int i1 = (int) (Math.random() * Barr.length + 1);
			int i2 = (int) (Math.random() * Barr.length + 1);

			tmp = Barr[i1];
			Barr[i1] = Barr[i2];
			Barr[i2] = tmp;
		}

		
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setSize(800, 800);
		frame.setLocationRelativeTo(null);
		frame.setVisible(true);
		frame.setLayout(new GridLayout(4, 4));

		for (int i = 0; i < Barr.length; i++) {
			frame.add(Barr[i]);
		}

		ActionListener listener = new ActionListener() {

			@Override
			public void actionPerformed(ActionEvent e) {

				JButton clickbtn = (JButton) e.getSource();
				;
				/*
				 * JOptionPane.showMessageDialog(frame, String.valueOf(clickbtn.getText()));
				 * JOptionPane.showMessageDialog(frame,
				 * clickbtn.getText().equals(String.valueOf(1)));
				 * 
				 */

				if (String.valueOf(i + 1).equals(clickbtn.getText())) {
					/*
					 * JOptionPane.showMessageDialog(frame, clickbtn.getText());
					 * JOptionPane.showMessageDialog(frame, String.valueOf(i+1));
					 */

					clickbtn.setEnabled(false);
					i++;

				} else {
					JOptionPane.showMessageDialog(frame, "LOSE");
					i = 0;
					for (int i = 0; i < Barr.length; i++) {
						Barr[i].setEnabled(true);
					}

				}
				if (i == Barr.length) {
					JOptionPane.showMessageDialog(frame, "WIN");
				}
			}

		};
		for (int i = 0; i < Barr.length; i++) {
			Barr[i].addActionListener(listener);
		}

	}
}

public class Homework02 {
	public static void main(String[] args) {
		NewFrame k = new NewFrame();
		k.PlayGame();

	}

}

```
