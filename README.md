# Aberdeen-3d-map-data

## Simple query

The basic building location data is sourced from open street map. This is achieved using the query tool at http://overpass-turbo.eu/, Handy Overpass QL guide / docs here -> http://wiki.openstreetmap.org/wiki/Overpass_API/Language_Guide#All_data_in_a_bounding_box 

Using a simple query like this:
  
    /*
    This query looks for nodes, ways and relations 
    with the given key/value combination.
    Choose your region and hit the Run button above!
    */
    [out:json][timeout:25];
    (
      way(57.1418796,-2.1119872,57.1491036,-2.0905636) -> .a;
     // <;
    );
    //out;
     
    
    // print results
    out geom;
    {{style:
      node, way, relation {
        /* text: name; */
      }
    /*node[man_made=surveillance] {
      color:black;
      fill-color:red;
      fill-opacity:1;
      symbol-size:3;
    }
    node[surveillance:type=camera] {
      fill-color:black;
    }*/
    }}
