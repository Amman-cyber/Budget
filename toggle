import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class DarkModeToggle {
    public static void main(String[] args) {
        // Create the main frame
        JFrame frame = new JFrame("Dark Mode Toggle");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(400, 300);
        frame.setLayout(new BorderLayout());

        // Create a panel to hold the button
        JPanel panel = new JPanel();
        panel.setLayout(new GridBagLayout());
        frame.add(panel, BorderLayout.CENTER);

        // Create the toggle button
        JButton toggleButton = new JButton("Light Mode");
        toggleButton.setFocusPainted(false);
        toggleButton.setBackground(Color.WHITE);
        toggleButton.setForeground(Color.BLACK);

        // Add shadow effect to the button
        toggleButton.setBorder(BorderFactory.createCompoundBorder(
                BorderFactory.createLineBorder(Color.GRAY, 2), // Outer shadow effect
                BorderFactory.createEmptyBorder(10, 20, 10, 20) // Padding inside the button
        ));

        // Add action listener for toggling dark mode
        toggleButton.addActionListener(new ActionListener() {
            private boolean isDarkMode = false;

            @Override
            public void actionPerformed(ActionEvent e) {
                if (isDarkMode) {
                    // Switch to Light Mode
                    panel.setBackground(Color.WHITE);
                    toggleButton.setText("Light Mode");
                    toggleButton.setBackground(Color.WHITE);
                    toggleButton.setForeground(Color.BLACK);
                    toggleButton.setBorder(BorderFactory.createCompoundBorder(
                            BorderFactory.createLineBorder(Color.GRAY, 2),
                            BorderFactory.createEmptyBorder(10, 20, 10, 20)
                    ));
                } else {
                    // Switch to Dark Mode
                    panel.setBackground(Color.DARK_GRAY);
                    toggleButton.setText("Dark Mode");
                    toggleButton.setBackground(Color.BLACK);
                    toggleButton.setForeground(Color.WHITE);
                    toggleButton.setBorder(BorderFactory.createCompoundBorder(
                            BorderFactory.createLineBorder(Color.LIGHT_GRAY, 2),
                            BorderFactory.createEmptyBorder(10, 20, 10, 20)
                    ));
                }
                isDarkMode = !isDarkMode;
            }
        });

        // Add the button to the panel
        panel.add(toggleButton);

        // Set frame visible
        frame.setVisible(true);
    }
}
