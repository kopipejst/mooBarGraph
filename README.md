mooBarGraph
===========

mooBarGraph AJAX graph plugin for Mootools.


How to use
----------

First you should create element in which you want to create graph. It can be something like:

<div id="myGraph"></div>

After that data array must be created. There are two types available: simple and stacked.

Array for simple type should be like this and everything exept value is optional:

	new graphData =  new Array(
		[value1,label1,color1,url1,tooltip1],
		[value2,label2,color2,url2,tooltip2],
		.....
		[valueN,labelN,colorN,urlN,tooltipN]
		);
		

For stacked type also only value is required and everything else is optional. It should look similar to next code:

	new graphData =  new Array(
		[[value11,value12,...,value1M],label1,color1,url1,tooltip1],
		[[value21,value22,...,value2M],label2,color2,url2,tooltip2],
		.....
		[[valueN1,valueN2,...,valueNM],labelN,colorN,urlN,tooltipN]
		);

After you create container and data you have to call mooBarGraph and pass values.

	window.addEvent('domready', function() {
	    var myGraph = new mooBarGraph({
	    	container: $('myGraph'),
	    	data: graphData
	    });
	})

This will be enought to create bar graph based on your data, but you can pass few additional options. List of all options is in next section.

Loading data via AJAX is easy. All you have to do is to call draw() function and pass url with data in JSON format.

	myGraph.draw(url);


mooBarGraph Options
-------------------

You should always have container and data options:

		container // element in which you want mooBarGraph to be created
		data // array of data for mooBarGraph
		
Other options are optional:

		width: 400 // width of graph panel in px
		height: 300 // height of graph panel in px
		barSpace: 10 // space between bars in px
		color: '#111111' // default color for your bars
		colors: false // array of colors for bars. it will be repeated.
		title: false // graph title. can use html tags 
		sort: false // 'asc' or 'desc'
		prefix: '' // string that will be show before bar value
		postfix: '' // string that will be shown after bar value
		legend: false // set to true if you want to lefend box be created
		legendWidth: 100 // width of legend box
		legends: false // array of values for legend
		showValues: true // for stacked bars type only. false to hide values in sub bars.
		showValuesColor: '#fff' // color for values in sub bars for stacked type
	


Screenshots
-----------


 