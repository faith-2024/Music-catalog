import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;
public class Musiccatalogueinterface {
    public static void main(String[] args) {
        // here is the boarderlayout
        JFrame frame = new JFrame("My music catalogue");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(500, 500);
        frame.setLayout(new BorderLayout());
        // here is north
        JLabel Label = new JLabel("My Music Catalogue", SwingConstants.CENTER);
        Label.setFont(new Font("Times New Roman", Font.BOLD, 22));
        frame.add(Label, BorderLayout.NORTH);
        // here is west
        String[] genre = {"Rap", "Reggae", "Ballads", "Hip-Hop", "Pop", "Rock & Roll"};
        JList<String> genreL = new JList<>(genre);
        frame.add(new JScrollPane(genreL), BorderLayout.WEST);
        // here is centre
        JPanel form = new JPanel(new GridLayout(4, 2, 2, 2));
        JLabel artistL = new JLabel("Artist Name:");
        JTextField artistF = new JTextField();
        JLabel studioL = new JLabel("Recording Studio:");
        JTextField studioF = new JTextField();
        JLabel categoryL = new JLabel("Category:");
        JComboBox<String> categoryC = new JComboBox<>(genre);
        JCheckBox available = new JCheckBox("Available");
        form.add(artistL);
        form.add(artistF);
        form.add(studioL);
        form.add(studioF);
        form.add(categoryL);
        form.add(categoryC);
        form.add(new JLabel(""));
        form.add(available);
        frame.add(form, BorderLayout.CENTER);
        // here is south
        JPanel button = new JPanel();
        JButton submit = new JButton("Submit");
        JButton exit = new JButton("Exit");
        submit.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                String artist = artistF.getText();
                String studio = studioF.getText();
                String category = (String) categoryC.getSelectedItem();
                boolean Available = available.isSelected();
                System.out.println("Artist: " + artist);
                System.out.println("Studio: " + studio);
                System.out.println("Category: " + category);
                System.out.println("Available: " + (Available ? "Yes" : "No"));
            }
        });
        exit.addActionListener(e -> System.exit(0));
        button.add(submit);
        button.add(exit);
        frame.add(button, BorderLayout.SOUTH);
        frame.setVisible(true);
    }
}
