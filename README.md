# Charts-react
import {useState} from 'react';
import './App.css';
import Chart from "react-apexcharts";


function App() {
const [charts,setCharts]= useState({
  colors:['#F44336', '#E91E63', '#9C27B0'],
  options: {
    chart: {
      id: "basic-bar"
    },
    xaxis: {
      categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998, 1999]
    }
  },
  series: [
    {
      name: "series-1",
      data: [30, 40, 45, 50, 49, 60, 70, 91]
    },
    
    {
      name: "series-2",
      data: [31, 41, 43, 51, 48, 61, 71, 96]
    }
  ]
})

  return (
    
       <div className="app">
            <Chart
              options={charts.options}
              series={charts.series}
              type="bar"
              width="500"
            />
             <Chart
              options={charts.options}
              series={charts.series}
              type="line"
              width="500"
            />
            
          </div>
    
  );
}

export default App;
