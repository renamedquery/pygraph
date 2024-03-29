.pygcs (Pygraph Color Sheet) File Parsing Instructions:
    PYGCS files are just json files with a different extension to make them easy to find.
    JSON files can be used as well as PYGCS files as long as they have the same format.
    The format is as follows:
        {
            "graphDataColors":[], // (LIST) used as the colors for each step of the graph; as the graph advances, so do the colors, for example, if this is set as ["HEX_FOR_WHITE", "HEX_FOR_GRAY", "HEX_FOR_BLACK"], the first line would be white, the second would be gray and the third black, the fourth would loop back to the first color and would be white, just as the fifth would be gray; to create looping colors then do things like ["HEX_FOR_WHITE", "HEX_FOR_GRAY", "HEX_FOR_BLACK", "HEX_FOR GRAY"] and this way it would loop from white to gray to black to gray to white nicely. (must contain a hex color codes with pound symbols at the beginnings)           
            "textSizeForCoordinates":15 // (INTEGER) used as the text size for coordinates on the graph, the text will appear next to any vertex on the plot of a line (if it equals 0 then text will not be drawn to the graph)
            "textSizeForTitles":15 // (INTEGER) used as the text size for titles on the graph, the text will appear on the top of the graph, and the sides of the X and Y graphs (if it equals 0 then the text will not be drawn to the graph)
            "backgroundColor":"#ffffff" // (STRING) used as the background color for the graph (must be a hex color code with a pound symbol at the beginning)
            "borderColor":"#000000" // (STRING) used as the color for the borders/outlines of the graph (must be a hex color code with a pound symbol at the beginning)
            "crosshairColor":"#000000" // (STRING) used as the color for the crosshairs of a linear graph (must be a hex color code with a pound symbol at the beginning)
            "titleColors":{ // (DICTIONARY) used as the colors for the titles for each axis
                "xAxis":"#0b0b0b", // (STRING) the color for the title(s) on the x axis (must be a hex color code with a pound symbol at the beginning)
                "yAxis":"#0b0b0b", // (STRING) the color for the title on the y axis (must be a hex color code with a pound symbol at the beginning)
                "graphTitle":"#0b0b0b", // (STRING) the color for the top title of the graph (must be a hex color code with a pound symbol at the beginning)
            }
        }
    If you are having trouble understanding this format, then raise an issue on the github repo for this project.
    An example of this format can be seen in the file "./grayscale.pygcs".