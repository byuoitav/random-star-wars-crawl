# Random Star Wars Crawls as a Service

### The Challenge

This is a challenge to gauge your skills and potential in software development.
For this challenge you will need to produce a service that will return
the opening "crawl" text from a random Star Wars film every time an endpoint is
hit. The requirements are as follows:
1. Your service should expose an HTTP endpoint on port `8080`
2. That HTTP endpoint should have a `/random_crawl` path that responds to a GET
request.
3. The `/random_crawl` endpoint should return a JSON formatted response as follows:
```json
{
	"film_name": "A New Hope",
	"opening_crawl": [
		"It is a period of civil war.",
		"Rebel spaceships, striking",
		"from a hidden base, have won",
		"their first victory against",
		"the evil Galactic Empire.",
		"",
		"During the battle, Rebel",
		"spies managed to steal secret",
		"plans to the Empire's",
		"ultimate weapon, the DEATH",
		"STAR, an armored space",
		"station with enough power",
		"to destroy an entire planet.",
		"",
		"Pursued by the Empire's",
		"sinister agents, Princess",
		"Leia races home aboard her",
		"starship, custodian of the",
		"stolen plans that can save her",
		"people and restore",
		"freedom to the galaxy...."
	]
}
```
4. Your service should dynamically get the opening crawl text from The Star Wars API (swapi.dev)
	* Note: The Star Wars API returns the opening crawl text as a single string with a carriage
	return and a new line (`\\r\\n`) separating the lines. This string needs to be broken up into
	an array of strings (one for each line) as seen above.
5. It is expected that your service will always successfully return a response every time it is
called as long as there are not problems with The Star Wars API.

You may use any language, framework, and libraries you would like in order to complete this challenge.

### Hints:

1. A reference service is included in the "Releases" portion of this repository. There is a service
built for Windows, Linux, and MacOS. You may download the service that corresponds to your OS of choice
and run it. It will expose a service on port `8080` of your localhost with a single `/random_crawl`
endpoint which will work as has been requested above. 
2. The Star Wars API contains six films with IDs 1-6. You may use these IDs directly to access a random
film from The Star Wars API.
3. All lines of the opening crawl are separated with the same substring (`\\r\\n`) in The Star Wars API.
This should make a standard library "String Split" function easy to use.


### Submission Instructions

Once your service is complete, please upload your code to a GitHub repository of your choosing.
Please create a README in the repository with instructions on how to compile and run your service.
Once you have done this, please email us a link to your repository.

