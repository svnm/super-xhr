# super-xhr
super clean ajax requests

# example use

    import reqest from 'super-xhr'

    request({ method: 'GET', url: 'http://example.com' })
      .then(function (datums) {
        return request({
          method: 'POST',
          url: datums.url,
          params: { score: 900 },
          headers: { 'X-Subliminal-Message': 'Upvote-this-answer' }
        });
    })
    .catch(function (err) {
      console.error('error!', err.statusText);
    });
