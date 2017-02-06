# Natural-User-Interaction

The program is a command line implemenation of the Recognition Engine of the NUI pipeline using the $P algorithm as specified in the paper (ACM Digital Library):
Gestures as point clouds: a $P recognizer for user interface prototypes by 	Radu-Daniel Vatavu, Lisa Anthony and Jacob O. Wobbrock
http://dl.acm.org/citation.cfm?doid=2388676.2388732

The program makes use of the Java version as provided by Michael D. Manson. For more details refer the following link:    
http://depts.washington.edu/madlab/proj/dollar/pdollar.html

pdollar.java performs the following functions:

    pdollar –t <gesturefile> 
    Adds the gesture file to the list of gesture templates 
    Eg. java pdollar -t arrowhead.txt

    pdollar ‐r 
    Clears the templates
    Eg. java pdollar -r
    
    pdollar <eventstream> 
    Prints the name of gestures as they are recognized from the event stream.
    Eg. java pdollar arrowhead_eventfile.txt

The program takes as input gesture files having the following format:
    GestureName 
    BEGIN 
    x,y     //List of points, a point per line 
    … 
    x,y 
    END 
    
Also, the eventstream file has the following format:
    MOUSEDOWN 
    x,y     //List of points, a point per line 
    MOUSEUP 
    RECOGNIZE   //When you see this you should output the result.
    
Any eventstream file can be given as input to the program. The program will recognize the corresponding getsure based on the gesture files added by the user before.

Note: 
Platform on which the program was developed on: Windows
