# My Atom snippets

```

'.source.js':
  'console.log':
    'prefix': 'lo'
    'body': 'console.log(\'$1\', $1);'

  'test:describe':
    'prefix': 'test:describe'
    'body': """
      describe('$1', () => {
        it('$2', () => {

          });
        });
    """

```
