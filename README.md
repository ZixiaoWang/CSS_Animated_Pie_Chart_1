# CSS_Animated_Pie_Chart_1
For Practise only.

Created by J,W.
12nd, Mar, 2016

#CSS Code
<code>

            .pie-chart.animation{
            
                width: 100px; 
                height: 100px; 
                border-radius: 50%;
                display: flex; 
                align-items: center;
                background-color: transparent;  
                position: absolute;
                left: 300px;
                z-index: 100;
                cursor: pointer;
                text-align: center;
                color: orange;
            }
            
            .pie-chart.animation::before,
            .pie-chart.animation::after{
                content:'';
                width: 100px; height: 100px;
                display: block;
                float: left;
                border-radius: 50%;
                position: absolute;
                top: 0px;
                left: 0px;
                border: 1px solid orange;
                
                animation-duration: 1s;
                animation-fill-mode: forwards;
            }
            .pie-chart.animation::after{
                clip: rect(0,102px,0px,51px);   
                animation-name: ff;
                animation-timing-function: ease-out;
            }
            .pie-chart.animation::before{
                clip:rect(102px, 51px,102px,0px);
                animation-name: bb;
                animation-timing-function: ease-out;
            }
            
            @keyframes ff{
                0% { clip: rect(0,102px,0px,51px);    }
                50% { clip: rect(0px,102px,102px,51px);   }
                100% { clip: rect(0px,102px,102px,51px);   }
            }
            @keyframes bb{
                0% { clip: rect(102px, 51px,102px,0px);    }
                50% { clip: rect(102px, 51px,102px,0px);    }
                100% { clip: rect(32px, 51px,102px,0px);   }
            }
</code>
