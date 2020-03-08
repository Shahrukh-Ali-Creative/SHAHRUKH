<html>

<head>
    <title>LAB TASK 7</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

</head>

<body>

    <script>
        var library = [
            {
                author: 'Bill Gates',
                title: 'The Road Ahead',
                readingStatus: true
            },
            {
                author: 'Steve Jobs',
                title: 'Walter Isaacson',
                readingStatus: true
            },
            {
                author: 'Suzanne Collins',
                title: 'Mockingjay: The Final Book of The Hunger Games',
                readingStatus: false
            }];
        console.log(library);
    </script>

    <form action="">
        <label>
            Radius: <input type="number" id="diameter"><br><br>
            Height: <input type="number" id="hoogte"> <br><br>
            <input type="button" value="volume of Cylinder" id="berekenBtn"><br><br>
            <input type="text" id="uitkomst">
        </label>
    </form>


    <script>
        window.addEventListener("DOMContentLoaded", function () {
            document.getElementById("berekenBtn").addEventListener("click", bereken);
        });

        function Cylinder(hoogte, diameter) {
            this.hoogte = hoogte;
            this.diameter = diameter;
        }

        Cylinder.prototype.volume = function () {
            var radius = this.diameter / 2;
            var hoogte = this.hoogte;

            var berekening = Math.PI * radius * radius * hoogte;
            return berekening;
        }


        function bereken() {
            var diameter = document.getElementById("diameter").value;
            var hoogte = document.getElementById("hoogte").value;
            var myCylinder = new Cylinder(diameter, hoogte);
            var result = myCylinder.volume();
            document.getElementById("uitkomst").value = result;
        }

    </script>
</body>

</html>
