// Normal user Regisration form

package javaform;
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
public class Form  extends JFrame implements ActionListener
{
	private Container c;
	private JLabel  title;
	//@Required
	private JLabel name;
	private JTextField tname;
	private JLabel mno;
	private JTextField tmno;
	private JLabel gender;
	private JRadioButton male;
	private JRadioButton female;
	private ButtonGroup gengp;
	private JLabel dob;
	private JComboBox date;
	private JComboBox month;
	private JComboBox year;
	private JLabel addr;
	private JTextArea taddr;
	private JCheckBox term;
	private JButton submit;
	private JButton reset;
	private JTextArea tout;
	private JLabel res;
	private JTextArea resadd;
	private String dates[]= {"1","2","3","4","5","6","7","8","9","10","11","12","13",
			                 "14","15","16","17","18","19","20","21","22","23","24",
			                 "25","26","27","28","29","30","31"};
	private String months[]= {"Jan","Feb","Mar","Apr","May","Jun","July","Aug","Sep","Oct","Nov","Dec"};
	private String years[]= {"2000","2001","2002","2003","2004","2005","2006","2007","2008","2009","2010",
			                 "2011","2012","2013","2014","2015","2016","2017","2018","2019","2020","2021"};
		
	public Form()  // constructor
	{
		
		/*setTitle("Registration form");
		setBounds(300,90,900,600);
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		//setResizable(false);
	    setSize(500,500);
		setVisible(true);*/
		
		c= getContentPane();
		setLayout(null);
		
		title= new JLabel("Registration Form");
		title.setFont(new Font("Times new Roman",Font.BOLD,30));
		title.setSize(300,30);
		title.setLocation(300,30);  
		c.add(title);
		
	//////////////////////////////////////////////////////////////////////////	
		
		name = new JLabel("Name");
		name.setFont(new Font("Times new Roman",Font.PLAIN,20));
		name.setSize(100,20);
		name.setLocation(100,100);
		c.add(name);
		
		tname = new JTextField();
		tname.setFont(new Font("Times new Roman",Font.PLAIN,15));
		tname.setSize(190,20);
		tname.setLocation(200,100);
		c.add(tname);
		
	////////////////////////////////////////////////////////////////////////	
		
		mno = new JLabel("Mobile");
		mno.setFont(new Font("Times new Roman",Font.PLAIN,20));
		mno.setSize(100,20);
		mno.setLocation(100,150); 
		c.add(mno);
		
		tmno = new JTextField();
		tmno.setFont(new Font("Times new Roman",Font.PLAIN,15));
		tmno.setSize(150,20);
		tmno.setLocation(200,150);;
		c.add(tmno);
		
   ////////////////////////////////////////////////////////////////////////	
		
		gender = new JLabel("Gender");
		gender.setFont(new Font("Times new Roman",Font.PLAIN,20));
		gender.setSize(100,20);
		gender.setLocation(100,200);;
		c.add(gender);
		
		male = new JRadioButton("Male");
		male.setFont(new Font("Times new Roman",Font.PLAIN,15));
		male.setSize(75,20);
		male.setLocation(200,200);
		male.setSelected(true);   // by default male 
		c.add(male);
		
		female = new JRadioButton("Female");
		female.setFont(new Font("Times new Roman",Font.PLAIN,15));
		female.setSize(80,20);
		female.setLocation(275,200);
		female.setSelected(false);
		c.add(female);
		
		gengp= new ButtonGroup();  // only one at a time would be selected
		gengp.add(male);
		gengp.add(female);
		
  ////////////////////////////////////////////////////////////////////////	
		
		dob = new JLabel("DOB");
		dob.setFont(new Font("Times new Roman",Font.PLAIN,20));
		dob.setSize(100,20);
	    dob.setLocation(100,250);
		c.add(dob);
		
		date = new JComboBox(dates);
		date.setFont(new Font("Times new Roman",Font.PLAIN,15));
		date.setSize(50,20);
		date.setLocation(200,250);
		c.add(date);
		
		month = new JComboBox(months);
		month.setFont(new Font("Times new Roman",Font.PLAIN,15));
		month.setSize(60,20);
	    month.setLocation(250,250);
		c.add(month);
		
		year = new JComboBox(years);
		year.setFont(new Font("Times new Roman",Font.PLAIN,15));
		year.setSize(60,20);
		year.setLocation(310,250);
		c.add(year);
		
  ////////////////////////////////////////////////////////////////////////	
		
		addr = new JLabel("Address");
		addr.setFont(new Font("Times new Roman",Font.PLAIN,20));
		addr.setSize(100,20);
	    addr.setLocation(100,300);
		c.add(addr);
		
		taddr = new JTextArea();  // no outline border in textArea
		taddr.setFont(new Font("Times new Roman",Font.PLAIN,15));
		taddr.setSize(250,70);
	    taddr.setLocation(200,300);
	    taddr.setLineWrap(true);   // if line get filled then start from next line
		c.add(taddr);
		
  ////////////////////////////////////////////////////////////////////////	
		
		term = new JCheckBox("Accept Terms And Conditions");
		term.setFont(new Font("Times new Roman",Font.PLAIN,15));
		term.setSize(250,20);
	    term.setLocation(150,400);
		c.add(term);
	
  ////////////////////////////////////////////////////////////////////////		
		
		submit = new JButton("Submit");
		submit.setFont(new Font("Times new Roman",Font.PLAIN,15));
		submit.setSize(100,20);
	    submit.setLocation(150,450);
	    submit.addActionListener(this);
		c.add(submit);
		
  ////////////////////////////////////////////////////////////////////////
		
		reset = new JButton("Reset");
		reset.setFont(new Font("Times new Roman",Font.PLAIN,15));
		reset.setSize(100,20);
	    reset.setLocation(270,450);
	    reset.addActionListener(this);
		c.add(reset);
		
  ////////////////////////////////////////////////////////////////////////
		
		tout = new JTextArea();
		tout.setFont(new Font("Times new Roman",Font.PLAIN,15));
		tout.setSize(300,400);
	    tout.setLocation(500,100);
	    tout.setLineWrap(true);  
	    tout.setEditable(false);
	    c.add(tout);
		
  ////////////////////////////////////////////////////////////////////////
	    
	    res = new JLabel("");
		res.setFont(new Font("Times new Roman",Font.PLAIN,20));
		res.setSize(500,25);
	    res.setLocation(100,500);
	    c.add(res);
		
	    
	    resadd = new JTextArea();  
		resadd.setFont(new Font("Times new Roman",Font.PLAIN,15));
		resadd.setSize(200,70);
	    resadd.setLocation(580,175);
	    resadd.setLineWrap(true);   
		c.add(resadd);
		
	}
	
	//actionPerformed() method is to get the action performed by the user and act accordingly
	public void actionPerformed(ActionEvent e)  // 'actionPerformed' is the function of "ActionListener interface"
	{
		if(e.getSource()==submit)
		{
			if(term.isSelected())  // if terms and conditions selected successfully
			{
				String data, data1, data2, data3;
				data= "Name: "+ tname.getText() + "\n" + "Mobile: " + tmno.getText() + "\n";
				
				if(male.isSelected())
					data1= "Gender: Male" + "\n";
				else  // if female is selected
					data1= "Gender: Female" + "\n";
				
				data2= "DOB: " + (String)date.getSelectedItem() + "/" + (String)month.getSelectedItem()
				                 + "/" + (String)year.getSelectedItem() + "\n";
				
				data3= "Address: " + taddr.getText();
				
				tout.setText(data + data1 + data2 + data3);
				tout.setEditable(false);
				res.setText("Registration Successful...");
			}
			
			else if(!term.isSelected())  // if terms and conditions not selected
			{
				tout.setText("");
				resadd.setText("");
				res.setText("Please accept terms and conditions...");
			}
			
		}
		
		else if(e.getSource()==reset)
		{
			String def="";  // if reset is selected then all the previous string will get replaced by new entered string
			tname.setText(def);
			tmno.setText(def);
			taddr.setText(def);
			res.setText(def);
			tout.setText(def);
			term.setSelected(false);
			date.setSelectedIndex(0);
			month.setSelectedIndex(0);
			year.setSelectedIndex(0);
			resadd.setText(def);
		}
	}
	
	public static void main(String[] args)
	{
		Form f1= new Form();
		f1.setBounds(300,90,900,600);
		f1.setSize(500,500);
		f1.setTitle("Registration form");
		//f1.setResizable(false);
		f1.setVisible(true);
		f1.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	}

}
