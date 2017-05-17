using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Catch_the_Button
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Button_MouseEnter(object sender, EventArgs e)
        {
            Random rang = new Random();
            var maxWidht = this.ClientSize.Width - Button.ClientSize.Width;
            var maxHeight = this.ClientSize.Height - Button.ClientSize.Height;
            this.Button.Location = new Point(rang.Next(maxWidht), rang.Next(maxHeight));

        }

        private void Button_Click(object sender, EventArgs e)
        {
            MessageBox.Show("Congratulations! " + " You Win!");
            
        }

        private void Button_LocationChanged(object sender, EventArgs e)
        {

        }

        private void Button_ClientSizeChanged(object sender, EventArgs e)
        {

        }
    }
}
