# ROHITH_8051
LIBRARY MANAGEMENT  SYSTEM
import javax.swing.*;
import java.awt.*;

import java.awt.event.*;

public class LibraryManagementSystem extends JFrame implements ActionListener {

    private static final long serialVersionUID = 1L;
  private JPanel mainPanel;
    private JLabel titleLabel, authorLabel, yearLabel;
    private JTextField titleTextField, authorTextField, yearTextField;
    private JButton addButton, searchButton, removeButton;
    private JTextArea bookListTextArea;

    public LibraryManagementSystem() {
        this.setTitle("Library Management System");
        this.setSize(500, 400);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
   mainPanel.add(titleLabel);

        titleTextField = new JTextField();
        mainPanel.add(titleTextField);

        authorLabel = new JLabel("Author:");
        mainPanel.add(authorLabel);

        authorTextField = new JTextField();
        mainPanel.add(authorTextField);

        mainPanel = new JPanel();
        mainPanel.setLayout(new GridLayout(5, 2));

        titleLabel = new JLabel("Title:");
       yearLabel = new JLabel("Year:");
        mainPanel.add(yearLabel);

        yearTextField = new JTextField();
        mainPanel.add(yearTextField);

        addButton = new JButton("Add Book");
        addButton.addActionListener(this);
        mainPanel.add(addButton);
      searchButton = new JButton("Search Book");
        searchButton.addActionListener(this);
        mainPanel.add(searchButton);

        removeButton = new JButton("Remove Book");
        removeButton.addActionListener(this);
        mainPanel.add(removeButton);

        bookListTextArea = new JTextArea();
        mainPanel.add(bookListTextArea);
              this.add(mainPanel);
        this.setVisible(true);
    }

    public static void main(String[] args) {
        new LibraryManagementSystem();
    }
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == addButton) {
            addBook();
        } else if (e.getSource() == searchButton) {
            searchBook();
        } else if (e.getSource() == removeButton) {
            removeBook();
        }
    }

    private void addBook() {
        String title = titleTextField.getText();
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == addButton) {
            addBook();
        } else if (e.getSource() == searchButton) {
            searchBook();
        } else if (e.getSource() == removeButton) {
            removeBook();
        }
    }

    private void addBook() {
        String title = titleTextField.getText();
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == addButton) {
            addBook();
        } else if (e.getSource() == searchButton) {
            searchBook();
        } else if (e.getSource() == removeButton) {
            removeBook();
        }
    }

     yearTextField.setText("");
    }

    private void searchBook() {
        String title = JOptionPane.showInputDialog(this, "Enter book title:");
        String[] books = bookListTextArea.getText().split("\n");
        for (String book : books) {
            if (book.startsWith(title)) {
                JOptionPane.showMessageDialog(this, book);
                return;
            }
        }
}
        JOptionPane.showMessageDialog(this, "Book not found.");
    }

    private void removeBook() {
        String title = JOptionPane.showInputDialog(this, "Enter book title:");
        String[] books = bookListTextArea.getText().split("\n");
        bookListTextArea.setText("");
        for (String book : books) {
      if (!book.startsWith(title)) {
                bookListTextArea.append(book + "\n");
            }
        }
    }
}



