# Dive Into Shortcodes

This repository contains the slide deck for the 2024 Dive Into Shortcodes presentation as well as some code snippets for the examples in the presentation.

This file contains the Lava examples by slide that should be easy to copy into an HTML block or Lava Tester. Examples are separated by slide title.

## The KPI Shortcode makes simple stats stand out

```liquid
{[ kpis ]}
    [[ kpi icon:'fa-paint-brush' value:'Value' color:'blue-600' ]][[ endkpi ]]
{[ endkpis ]}
```

## Get a flat look by removing the card border and icon background

```liquid
{[ kpis style:'edgeless' iconbackground:'false' ]}
    [[ kpi labellocation:'top' ]][[ endkpi ]]
{[ endkpis ]}
```

## Easy updates to KPI width and height

```liquid
{[ kpis size:'sm' columncount:'6' ]}
    [[ kpi icon:'fa-paint-brush' value:'Small (sm)' label:'Column Count: 6' color:'blue-600' ]][[ endkpi ]]
{[ endkpis ]}
```

## KPIs accept the icon type class in the kpis tag and the icon class in the kpi items

```liquid
{[ kpis icontype:'fa-duotone' ]}
    [[ kpi icon:'fa-paint-brush' ]]
{[ endkpis ]}
```

## Panels create simple visual boundaries

```liquid
{[ panel icon:'fa fa-users' title:'User Information' ]}
    ...Content...
{[ endpanel]}
```

## Panel types can change the way a panel is displayed

```liquid
{[ panel type:'default' ]}
    ...Content...
{[ endpanel]}
```

```liquid
{[ panel type:'widget' ]}
    ...Content...
{[ endpanel]}
```

```liquid
{[ panel type:'block' ]}
    ...Content...
{[ endpanel]}
```

## Panel types can change a panel's color

```liquid
{[ panel type:'primary' ]}
    ...Content...
{[ endpanel]}
```

```liquid
{[ panel type:'success' ]}
    ...Content...
{[ endpanel]}
```

```liquid
{[ panel type:'warning' ]}
    ...Content...
{[ endpanel]}
```

```liquid
{[ panel type:'danger' ]}
    ...Content...
{[ endpanel]}
```

## Trend Charts provide a clear visual without the extra clutter of a full chart

```liquid
{[ trendchart ]}
    [[ dataitem label:'Label' value:'100' color:'#74AF6E' ]][[ enddataitem ]]
{[ endtrendchart ]}
```

## Charts are powerful and diverse data visualization tools

```liquid
{[ chart type:'bar' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'horizontalBar' labels:'June,July,August' legendshow:'true' chartheight:'200px' valueformat:'none' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'stackedbar' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'rgba(0,0,0,0)' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'rgba(0,0,0,0)' pointbordercolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'radar' labels:'June,July,August' chartheight:'200px' xaxisshow:'false' yaxisshow:'false' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

## There are three types of bar chart you can use

```liquid
{[ chart type:'bar' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'horizontalBar' labels:'June,July,August' legendshow:'true' chartheight:'200px' valueformat:'none' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'stackedbar' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'bar' chartheight:'200px' xaxistype:'time' ]}
    [[ dataitem label:'6/1/2024' value:'215' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
    [[ dataitem label:'7/1/2024' value:'137' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
    [[ dataitem label:'8/1/2024' value:'374' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
{[ endchart ]}
```

## There is one type of line chart that can be customized in many ways

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' curvedlines:'false' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' curvedlines:'false' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' fillcolor:'#FE5F55' filllinearea:'true' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' fillcolor:'#84E6F8' filllinearea:'true' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'rgba(0,0,0,0)' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'rgba(0,0,0,0)' pointbordercolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

## Charts with singular configurations

```liquid
{[ chart type:'doughnut' labels:'Small Groups' chartheight:'200px' legendshow:'true' xaxisshow:'false' yaxisshow:'false' legendposition:'top' ]}
    [[ dataitem label:'June' value:'215' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
    [[ dataitem label:'July' value:'137' fillcolor:'#84E6F8' ]] [[ enddataitem ]]
    [[ dataitem label:'August' value:'374' fillcolor:'#9381FF' ]] [[ enddataitem ]]
{[ endchart ]}
```

```liquid
{[ chart type:'pie' labels:'Small Groups' chartheight:'200px' legendshow:'true' xaxisshow:'false' yaxisshow:'false' legendposition:'top' ]}
    [[ dataitem label:'June' value:'215' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
    [[ dataitem label:'July' value:'137' fillcolor:'#84E6F8' ]] [[ enddataitem ]]
    [[ dataitem label:'August' value:'374' fillcolor:'#9381FF' ]] [[ enddataitem ]]
{[ endchart ]}
```

```liquid
{[ chart type:'radar' labels:'June,July,August' chartheight:'200px' xaxisshow:'false' yaxisshow:'false' legendshow:'true'  legendposition:'right' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' pointcolor:'#FE5F55' pointbordercolor:'#FE5F55' bordercolor:'#FE5F55' fillcolor:'#FE5F55' ]] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' pointcolor:'#84E6F8' bordercolor:'#84E6F8' pointbordercolor:'#84E6F8' fillcolor:'#84E6F8' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'polarArea' labels:'June,July,August' chartheight:'200px' xaxisshow:'false' yaxisshow:'false' ]}            
    [[ dataitem label:'June' value:'215' fillcolor:'#FE5F55' ]] [[ enddataitem ]]
    [[ dataitem label:'July' value:'137' fillcolor:'#84E6F8' ]] [[ enddataitem ]]
    [[ dataitem label:'August' value:'374' fillcolor:'#9381FF' ]] [[ enddataitem ]]
{[ endchart ]}
```

## Chart data can be configured two ways

```liquid
{[ chart type:'bar' ]}
    [[ dataitem label:'June' value:'200' ]] [[ enddataitem ]]
    [[ dataitem label:'July' value:'220' ]] [[ enddataitem ]]
{[ endchart ]}
```

```liquid
{[ chart type:'bar' labels:'June, July, August' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374']] [[ enddataset ]]
    [[ dataset label:'Serving Teams' data:'200, 220, 314' ]] [[ enddataset ]]
{[ endchart ]}
```

## Chart colors are configured differently depending on the type of chart

```liquid
{[ chart type:'bar' labels:'June,July,August' legendshow:'true' chartheight:'200px' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374'  ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'line' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'radar' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'pie' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'doughnut' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]] [[ enddataset ]]
{[ endchart ]}
```

```liquid
{[ chart type:'polarArea' labels:'June,July,August' legendshow:'true' chartheight:'200px' ]}
    [[ dataset label:'Small Groups' data:'215, 137, 374' fillcolor:'#FE5F55' bordercolor:'#84E6F8' pointcolor:'#9381FF' pointbordercolor:'#B2D373' pointborderwidth:'3' pointradius:'5' borderwidth:'3' ]] [[ enddataset ]]
{[ endchart ]}
```

## Scheduled Content

```liquid
{[ scheduledcontent scheduleid:'123' ]}
    ...Content...
{[ endscheduledcontent ]}
```

## Conditional Rendering Based on Schedule

```liquid
{[ scheduledcontent scheduleid:'2729' ]}
    {[ mediaplayer media:'113' ]}{[ endmediaplayer ]}
{[ endscheduledcontent ]}
{[ scheduledcontent scheduleid:'2729' showwhen:'notlive' ]}
    {[ mediaplayer media:'112' ]}{[ endmediaplayer ]}
{[ endscheduledcontent ]}
```

## Scheduled Content has Merge Fields Available

```liquid
{[ scheduledcontent scheduleid:'1234' showwhen:'both' ]}
    {% if IsLive == true %}
        {[ mediaplayer media:'113' ]}{[ endmediaplayer ]}
        Service ends at {{ OccurrenceEndDateTime | 'st' }}
    {% else %}
        Join us on {{ NextOccurrenceDateTime | Date:'dddd' }}!  
    {% endif %}
{[ endscheduledcontent ]}
```

## Media Player

```liquid
{[ mediaplayer media:'112' ]}{[ endmediaplayer ]}
```

```liquid
{[ mediaplayer src:'https://www.youtube.com/watch?v=dQw4w9WgXcQ' ]}{[ endmediaplayer ]}
```

## The Order of Controls Will Determine How They are Displayed

```liquid
{[ mediaplayer media:'112' controls:'play,fast-forward,progress,rewind,mute,volume,fullscreen' ]}{[ endmediaplayer ]}
```

## Google Maps

```liquid
{[ googlemap ]}
    [[ marker location:'38.9116785,-92.3174238' title:'The Crossing']][[ endmarker ]]
{[ endgooglemap ]}
```

## Map and Markers Can be Styled

```liquid
{[ googlemap ]}
    [[ marker location:'38.9116785,-92.3174238' 
       icon:'https://linkToMyIcon']][[ endmarker ]]
    [[ style ]]
        [ JSON For Map Style ]
    [[ endstyle ]]
{[ endgooglemap ]}
```

## The Current Markup

```html
<div id="carouselExample" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    {% for slide in slides %}
        <li data-target="#carouselExample" data-slide-to="{{forloop.index0}}" 
            {% if forloop.first == true %}class="active"{% endif %}></li>
    {% endfor %}
  </ol>
  <div class="carousel-inner">
    {% for slide in slides %}
        <div class="carousel-item item {% if forloop.first == true %}active{% endif %}">
            <img class="d-block w-100" src="{{ slide.src }}" alt="{{ slide.title }}">
            <div class="carousel-caption d-none d-md-block"><p>{{ slide.content }}</p></div>
        </div>
    {% endfor %}
  </div>
</div>
<script> $(document).ready(() => { $('.carousel').carousel(); }); </script>
```

## Using the Shortcode

```liquid
{[ carousel ]} 
    [[ slide title:'Bear Slide' src:'https://placebear.com/600/200' ]]
        Bear Scares!
    [[ endslide ]]
    [[ slide title:'Another Bear Slide' src:'https://placebear.com/300/100' ]]
        Another bear!
    [[ endslide ]]
{[ endcarousel ]}
```

## Resolve Conflicts With a Parameter

```html
<div id="{{ carouselid }}" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    {% for slide in slides %}
        <li data-target="#{{ carouselid }}" data-slide-to="{{forloop.index0}}" 
            {% if forloop.first == true %}class="active"{% endif %}></li>
    {% endfor %}
  </ol>
```

```liquid
{[ carousel carouselid:'bear-scares' ]} 
    [[ slide title:'Bear Slide' src:'https://placebear.com/600/200' ]]
        Bear Scares!
    [[ endslide ]]
    [[ slide title:'Another Bear Slide' src:'https://placebear.com/300/100' ]]
        Another bear!
    [[ endslide ]]
{[ endcarousel ]}
```
