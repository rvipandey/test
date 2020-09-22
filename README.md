# test

<script src="https://code.highcharts.com/highcharts.js"></script>
<script src="https://code.highcharts.com/modules/sankey.js"></script>
<script src="https://code.highcharts.com/modules/exporting.js"></script>
<script src="https://code.highcharts.com/modules/export-data.js"></script>
<script src="https://code.highcharts.com/modules/accessibility.js"></script>

<figure class="highcharts-figure">
  <div id="container"></div>
  <p class="highcharts-description">
    Sankey charts are used to visualize data flow and volume
    between nodes. The wider lines indicate larger volumes.
  </p>
</figure>


#csv {
	display: none;
}

.highcharts-figure, .highcharts-data-table table {
  min-width: 310px;
  max-width: 800px;
  margin: 1em auto;
}

.highcharts-data-table table {
	font-family: Verdana, sans-serif;
	border-collapse: collapse;
	border: 1px solid #EBEBEB;
	margin: 10px auto;
	text-align: center;
	width: 100%;
	max-width: 500px;
}
.highcharts-data-table caption {
  padding: 1em 0;
  font-size: 1.2em;
  color: #555;
}
.highcharts-data-table th {
	font-weight: 600;
  padding: 0.5em;
}
.highcharts-data-table td, .highcharts-data-table th, .highcharts-data-table caption {
  padding: 0.5em;
}
.highcharts-data-table thead tr, .highcharts-data-table tr:nth-child(even) {
  background: #f8f8f8;
}
.highcharts-data-table tr:hover {
  background: #f1f7ff;
}


--script--


Highcharts.chart('container', {

  title: {
    text: 'Highcharts Sankey Diagram'
  },
  accessibility: {
    point: {
      valueDescriptionFormat: '{index}. {point.from} to {point.to}, {point.weight}.'
    }
  },
  series: [{
    keys: ['from', 'to', 'weight'],
    data: [
      ['Brazil', 'Portugal', 5],
      ['Brazil', 'France', 1],
      ['Brazil', 'Spain', 1],
      ['Brazil', 'England', 1],
      ['Canada', 'Portugal', 1],
      ['Canada', 'France', 5],
      ['Canada', 'England', 1],
      ['Mexico', 'Portugal', 1],
      ['Mexico', 'France', 1],
      ['Mexico', 'Spain', 5],
      ['Mexico', 'England', 1],
      ['USA', 'Portugal', 1],
      ['USA', 'France', 1],
      ['USA', 'Spain', 1],
      ['USA', 'England', 5],
      ['Portugal', 'Angola', 2],
      ['Portugal', 'Senegal', 1],
      ['Portugal', 'Morocco', 1],
      ['Portugal', 'South Africa', 3],
      ['France', 'Angola', 1],
      ['France', 'Senegal', 3],
      ['France', 'Mali', 3],
      ['France', 'Morocco', 3],
      ['France', 'South Africa', 1],
      ['Spain', 'Senegal', 1],
      ['Spain', 'Morocco', 3],
      ['Spain', 'South Africa', 1],
      ['England', 'Angola', 1],
      ['England', 'Senegal', 1],
      ['England', 'Morocco', 2],
      ['England', 'South Africa', 7],
      ['South Africa', 'China', 5],
      ['South Africa', 'India', 1],
      ['South Africa', 'Japan', 3],
      ['Angola', 'China', 5],
      ['Angola', 'India', 1],
      ['Angola', 'Japan', 3],
      ['Senegal', 'China', 5],
      ['Senegal', 'India', 1],
      ['Senegal', 'Japan', 3],
      ['Mali', 'China', 5],
      ['Mali', 'India', 1],
      ['Mali', 'Japan', 3],
      ['Morocco', 'China', 5],
      ['Morocco', 'India', 1],
      ['Morocco', 'Japan', 3]
    ],
    type: 'sankey',
    name: 'Sankey demo series'
  }]

});


