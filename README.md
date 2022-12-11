# Week-7-Programming
Week 7 Programming Code

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Module6MethodsProjectDL
{
    public partial class frmRealID : Form
    {
        // Public Contsants to use
        const byte ADD = 0;
        const byte SUBTRACT = 1;
        const byte MULTIPLY = 2;
        const byte DIVIDE = 3;
        const byte MODULUS = 4;

        public frmRealID()
        {
            InitializeComponent();
        }

        //Put Your method here

        private void btn5_Click(object sender, EventArgs e)

        {
            decimal dLeft = 0.0m;
            decimal dRight = 0.0m;
            decimal dAnswer = 0.0m;
            string szLeft = "";
            string szRight = "";
            string szAnswer = "";
            string szEquation = "";


            try
            {
                szLeft = textBox2.Text;
                szRight = textBox1.Text;


                dLeft = Convert.ToDecimal(szLeft);

                dRight = Convert.ToDecimal(szRight);


                dAnswer = dLeft % dRight;

                szAnswer = dAnswer.ToString();

                szEquation = szLeft + " % " + szRight + " = " + szAnswer;


                label3.Text = "";
                label3.Text = szEquation;

                if (dLeft < 0 || dRight < 0)
                    label3.Text = "No negative numbers during an Modulus Operation";
            }
            catch (FormatException)
            {

                label3.Text = "Numeric Numbers Only.";
                if (textBox2.Text == "" || textBox1.Text == "")
                    label3.Text = "Please enter a valid number in both textboxs.";


            }










        }


        private void btn4_Click(object sender, EventArgs e)
        {
            decimal dLeft = 0.0m;
            decimal dRight = 0.0m;
            decimal dAnswer = 0.0m;
            string szLeft = "";
            string szRight = "";
            string szAnswer = "";
            string szEquation = "";

            try
            {
                szLeft = textBox2.Text;
                szRight = textBox1.Text;

                dLeft = Convert.ToDecimal(szLeft);
                dRight = Convert.ToDecimal(szRight);

                dAnswer = dLeft / dRight;

                szAnswer = dAnswer.ToString();

                szEquation = szLeft + " / " + szRight + " = " + szAnswer;

                label3.Text = "";
                label3.Text = szEquation;
            }
            catch (DivideByZeroException)
            {
                label3.Text = "You can not divide by zero.";
            }
            catch (FormatException)
            {

                label3.Text = "Numeric Numbers Only.";
                if (textBox2.Text == "" || textBox1.Text == "")
                    label3.Text = "Please enter a valid number in both textboxs.";
            }
        }

        private void btn3_Click(object sender, EventArgs e)
        {
            decimal dLeft = 0.0m;
            decimal dRight = 0.0m;
            decimal dAnswer = 0.0m;
            string szLeft = "";
            string szRight = "";
            string szAnswer = "";
            string szEquation = "";
            try
            {
                szLeft = textBox2.Text;
                szRight = textBox1.Text;


                dLeft = Convert.ToDecimal(szLeft);
                dRight = Convert.ToDecimal(szRight);

                dAnswer = dLeft * dRight;

                szAnswer = dAnswer.ToString();

                szEquation = szLeft + " * " + szRight + " = " + szAnswer;

                label3.Text = "";
                label3.Text = szEquation;
            }
            catch (FormatException)
            {

                label3.Text = "Numeric Numbers Only.";
                if (textBox2.Text == "" || textBox1.Text == "")
                    label3.Text = "Please enter a valid number in both textboxs.";
            }

        }

        private void btn2_Click(object sender, EventArgs e)
        {
            decimal dLeft = 0.0m;
            decimal dRight = 0.0m;
            decimal dAnswer = 0.0m;
            string szLeft = "";
            string szRight = "";
            string szAnswer = "";
            string szEquation = "";
            try
            {
                szLeft = textBox2.Text;
                szRight = textBox1.Text;

                dLeft = Convert.ToDecimal(szLeft);
                dRight = Convert.ToDecimal(szRight);

                dAnswer = dLeft - dRight;

                szAnswer = dAnswer.ToString();

                szEquation = szLeft + " - " + szRight + " = " + szAnswer;

                label3.Text = "";
                label3.Text = szEquation;
            }
            catch (FormatException)
            {

                label3.Text = "Numeric Numbers Only.";
                if (textBox2.Text == "" || textBox1.Text == "")
                    label3.Text = "Please enter a valid number in both textboxs.";
            }

        }

        private void btn1_Click(object sender, EventArgs e)
        {
            decimal dLeft = 0.0m;
            decimal dRight = 0.0m;
            decimal dAnswer = 0.0m;
            string szLeft = "";
            string szRight = "";
            string szAnswer = "";
            string szEquation = "";
            try
            {
                szLeft = textBox2.Text;
                szRight = textBox1.Text;

                dLeft = Convert.ToDecimal(szLeft);
                dRight = Convert.ToDecimal(szRight);

                dAnswer = dLeft + dRight;

                szAnswer = dAnswer.ToString();

                szEquation = szLeft + " + " + szRight + " = " + szAnswer;

                label3.Text = "";
                label3.Text = szEquation;
            }
            catch (FormatException)
            {

                label3.Text = "Numeric Numbers Only.";
                if (textBox2.Text == "" || textBox1.Text == "")
                    label3.Text = "Please enter a valid number in both textboxs.";



            }

        }

        private void lbl1_Click(object sender, EventArgs e)
        {

        }

        private void lbl2_Click(object sender, EventArgs e)
        {

        }

        private void txtBox2_TextChanged(object sender, EventArgs e)
        {




        }

        private void txtBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void lbl3_Click(object sender, EventArgs e)
        {

        }

        private void btn6_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        
    }
}
