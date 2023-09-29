## Bucket erstellen
Als allererstes erstellen wir einen neuen Bucket in S3 mit:
+ Uniquer Name
+ All Public (Bestätigung unten Bestätigen)
Wenn wir das haben, können wir unser Bucket createn.

So, kurz darauf gehen wir in unsere Bucket Sicht
![Permission](Permission%20Bucket.png)

Bisschen weiter unten steht "Bucket Policy" und wir fügen dann diesen Code hier ein:
~~~
{
	"Version":"2012-10-17",
	"Statement":[
		{
			"Sid":"PublicReadGetObject"
			"Effect":"Allow",
			"Principal":"*",
			"Action":[
				"s3:GetObject"

			],
			"Resource":[

				"arn:aws:s3:::stepankova/*"
			]
		}
	]
}
~~~