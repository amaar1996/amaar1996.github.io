<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no">
  <link rel="stylesheet" href="./css/style.css">
  <link rel="stylesheet" href="http://js.arcgis.com/4.3/esri/css/main.css">
  <script src="https://js.arcgis.com/4.3/"></script>
  <title> madinah map </title>
</head>
<body>
        <header>
                <div class="container">
                    <div id="branding">
                         <h2>البنية التحتية للبيانات المكانية للمدينة المنورة  </h2>
                    </div>
                    <nav>
                        <ul>
                            <li><a href="#">         الصفحة الرئيسية          </a></li>
                            <li><a href="#">             عن المركز             </a></li>
                            <li><a href="#">             الشركاء               </a></li>
                            <li><a href="#">         أعضاء اللجنة الفنية      </a></li>
                            <li><a href="#">          الأخبار والفعاليات       </a></li>  
                        </ul>
                    </nav>
                </div>
            </header>
            <section>
            <div id="viewDiv"></div>
            <div id="search"></div>
            <style>
                     #viewDiv {
                      border: solid;
                      margin: center;
                      width: auto;
                      height: 550px;
                    }
                  </style>
                    <script>  
                    require([
                      "esri/Map",
                      "esri/views/MapView",
                    ], function(Map, MapView) {

                      var map = new Map({
                        basemap: "topo-vector"
                      });
                
                      var view = new MapView({
                        container: "viewDiv",
                        map: map,
                        center: [39.610070,24.468876],
                        zoom: 15
                      });
                      var search = new Search({
                      map: map,
                      }, dom.byId("search"));
                      search.startup();
                    });
                  </script>
                  </section>
                  </div>
</html>
