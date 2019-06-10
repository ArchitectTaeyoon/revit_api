using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Autodesk.DesignScript.Runtime;
using Autodesk.DesignScript.Interfaces;
using Autodesk.DesignScript.Geometry;


namespace MyTestUI
{
    class UItesting
    {
        public List<Object> UI_Interface(double min, double max, List<Object> list)
        {
            List<Object> listReturn = new List<object>();
            MyTestUI window = new MyTestUI();

            //Slider
            window.slider.Maximum = max;
            window.slider.Minimum = min;

            //combobox
            window.combobox.ItemsSource = list;

            var res = window.ShowDialog();
            if (!res.HasValue && res.Value)
                window.Close();

            var data = window.combobox.SelectedItem;
            listReturn.Add(data);
            listReturn.Add(window.text1.Text);
            listReturn.Add(window.slider.Value.ToString());
            return listReturn;
        }
    }
}
