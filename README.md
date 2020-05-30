$ go-grab-xkcd --help

Usage of go-grab-xkcd:
  -n int
        Comic number to fetch (default latest)
  -o string
        Print output in format: text/json (default "text")
  -s    Save image to current directory
  -t int
        Client timeout in seconds (default 30)
        
        
        
Usage on the command Line:

$ go-grab-xkcd -n 323

Title: Ballmer Peak
Comic No: 323
Date: 1-10-2007
Description: Apple uses automated schnapps IVs.
Image: https://imgs.xkcd.com/comics/ballmer_peak.png


$ go-grab-xkcd -n 323 -o json
{
  "title": "Ballmer Peak",
  "number": 323,
  "date": "1-10-2007",
  "description": "Apple uses automated schnapps IVs.",
  "image": "https://imgs.xkcd.com/comics/ballmer_peak.png"
}



Files in the app.
go.mod - Go Modules file used in Go for package management
main.go - Main entrypoint of the application
comic.go - Go representation of the data as a struct and operations on it
xkcd.go - xkcd client for making HTTP calls to the API, parsing response and saving to disk
