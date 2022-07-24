import java.awt.*;
import java.util.*;
import javax.swing.*;

@SuppressWarnings("serial")
public class CreatBean extends JPanel {
Image img;

        public CreatBean() {
        	
            img = new ImageIcon("Beans.png").getImage();
        }

        public void paintComponent(Graphics g) {
            Graphics2D g2d = (Graphics2D) g;
            g2d.translate(0, 0);
            g2d.drawImage(img, 0, 0, this);
        }

        public static void main(String[] args) {
        	// change to make more\less noticeable
        	int p = 10;
        	Random ran = new Random();
        	
        	while (true) {
        		try { 
        			 
        			
        			int x = ran.nextInt(1600);
        			int y = ran.nextInt(900);
        			
		            JFrame frame = new JFrame("BEANS!");
		            CreatBean panel = new CreatBean();
		            		
		            frame.setContentPane(panel);
		            frame.setResizable(false);
		            frame.setSize(500,500);
		            frame.setLocation(x,y);
		            frame.setVisible(true);
		            
		            Thread.sleep(p);
		            
		            if (p> 10) {
		            	p -=10;
		            }
		            
	            } catch (Exception e) {
	            	
	            }
        	}
    }
}
