package holaam;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JList;
import javax.swing.JTextField;
import javax.swing.JLabel;
import javax.swing.DefaultListModel;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.border.LineBorder;
import java.awt.Color;
import javax.swing.event.ListSelectionListener;
import javax.swing.event.ListSelectionEvent;
import java.awt.Toolkit;

public class bbbb {

	private JFrame frmLista;
	private JList lstNombres;
	private JTextField txtNombre;
	private JButton btnAgregar;
	private JLabel lblNewLabel;
	DefaultListModel model=new DefaultListModel();
	private JButton btnBorrar;
	private JLabel lblHola;

	
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					bbbb window = new bbbb();
					window.frmLista.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	
	public bbbb() {
		initialize();
	}

	
	private void initialize() {
		frmLista = new JFrame();
		frmLista.setIconImage(Toolkit.getDefaultToolkit().getImage(bbbb.class.getResource("/holaam/cecytem-logo-57EA94498B-seeklogo.com.png")));
		frmLista.setTitle("Lista");
		frmLista.setBounds(100, 100, 526, 348);
		frmLista.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frmLista.setLocationRelativeTo(null);
		frmLista.getContentPane().setLayout(null);
		
		lstNombres = new JList();
		lstNombres.addListSelectionListener(new ListSelectionListener() {
			public void valueChanged(ListSelectionEvent e) {
				lblHola.setText("hola"+lstNombres.getSelectedValue());
				
			}
		});

		lstNombres.setBounds(23, 105, 203, 169);
		frmLista.getContentPane().add(lstNombres);
		
		txtNombre = new JTextField();
		txtNombre.setBounds(99, 36, 86, 20);
		frmLista.getContentPane().add(txtNombre);
		txtNombre.setColumns(10);
		
		lblNewLabel = new JLabel("Nombre");
		lblNewLabel.setBounds(48, 39, 46, 14);
		frmLista.getContentPane().add(lblNewLabel);
		
		btnAgregar = new JButton("Agregar");
		btnAgregar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				model.addElement(txtNombre.getText());
				lstNombres.setModel(model);
			}
		});
		btnAgregar.setBounds(23, 67, 89, 23);
		frmLista.getContentPane().add(btnAgregar);
		
		btnBorrar = new JButton("Borrar");
		btnBorrar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				txtNombre.setText("");
				model.clear();
				lblHola.setText("");

			}
		});
		btnBorrar.setBounds(133, 67, 89, 23);
		frmLista.getContentPane().add(btnBorrar);
		
		lblHola = new JLabel("");
		lblHola.setBorder(new LineBorder(new Color(0, 0, 0), 4, true));
		lblHola.setBounds(267, 67, 193, 128);
		frmLista.getContentPane().add(lblHola);
	}

}
