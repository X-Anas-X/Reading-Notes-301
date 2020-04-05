# _SuperAgent:_
- SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs.
-  request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
   
   * A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request.
   
   ## Setting header fields:
   >* Setting header fields is simple, invoke .set() with a field name and value:

 request
   .get('/search')
   .set('API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(callback);
   
  + The .query() method accepts objects, which when used with the GET method will form a query-string. The following will produce the path /search?query=Manny&range=1..5&order=desc.
  
  ## Retrying requests
  - When given the .retry() method, SuperAgent will automatically retry requests, if they fail in a way that is transient or could be due to a flaky Internet connection.

  - This method has two optional arguments: number of retries (default 3) and a callback. It calls callback(err, res) before each retry. The callback may return true/false to control whether the request sould be retried (but the maximum number of retries is always applied).
