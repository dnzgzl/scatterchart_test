<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <script
            src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.6.0/Chart.min.js">
    </script>

    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <title>scattertry</title>
</head>

<body>
<div class = "container">
    <label for="x-Achse">x-Achse:</label>
    <select id ="selectid1" name= "x-Achse">
        <option value = "xv1"> placeholder x1</option>
        <option value = "xv2"> placeholder x2</option>
    </select>

    <label for="y-Achse">y-Achse:</label>
    <select id ="selectid2" name= "y-Achse">
        <option value = "yv1">placeholder y1</option>
        <option value = "yv2">placeholder y2</option>
    </select>

    <label for="kreis">Kreis:</label>
    <select id="selectid3" name= "kreis">
        <option>dynamische Größe AUS</option>
        <option>option1</option>
        <option>option2</option>
        <option>option3</option>
    </select>
    <br></br>
    <label for="regr">Regression:</label>
    <select id="selectid4" name= "regression">
        <option>an</option>
        <option>aus</option>
    </select>

    <label for="anima">Animation</label>
    <select id= "selectid5" name= "Animation">
        <option>Platzhalter x1</option>
        <option>Platzhalter x2</option>
    </select>

    <label for="time">Zeit:</label>
    <select id="selectid6" name= "zeit">
        <option>Platzhalter x1</option>
        <option>Platzhalter x2</option>
    </select>

    <canvas id = "meinChart"></canvas>
</div>
<script>
    (function(window, document, undefined) {
            var chart_data = {
            labels: "ScatterChart",
            datasets: [
                {
                    label: ["Team 1"],
                    backgroundColor: "rgba(255,221,50,0.2)",
                    borderColor: "rgba(255,221,50,1)",
                    data: [{
                        x: 21269017,
                        y: 21456783,
                    }]
                }, {
                    label: ["Team 2"],
                    backgroundColor: "rgba(60,186,159,0.2)",
                    borderColor: "rgba(60,186,159,1)",
                    data: [{
                        x: 258702,
                        y: 234558,
                    }]
                }, {
                    label: ["Team 3"],
                    backgroundColor: "rgba(0,0,0,0.2)",
                    borderColor: "#000",
                    data: [{
                        x: 3979083,
                        y: 1234455,
                    }]
                }, {
                    label: ["Team 4"],
                    backgroundColor: "rgba(193,46,12,0.2)",
                    borderColor: "rgba(193,46,12,1)",
                    data: [{
                        x: 4931877,
                        y: 3456789,
                    }]
                }
            ]}

            var meinChart = document.getElementById('meinChart').getContext('2d');
            window.primeAcChart = new Chart(meinChart, ( {
                type: 'scatter', //'bubble',
                data: chart_data,
                options: {
                    title: {
                        display: true,
                        text: 'Vergleich Werbungskosten / Umsatz'
                    }, scales: {
                        yAxes: [{
                            scaleLabel: {
                                display: true,
                                labelString: 'Umsatz(€)'
                            }
                        }],
                        xAxes: [{
                            scaleLabel: {
                                display: true,
                                labelString: 'Werbungskosten (€)'
                            }
                        }]
                    },
                    responsive: true,
                    showLines: true,
                }

            }))
    })(window, document)


</script>
</body>
</html>
