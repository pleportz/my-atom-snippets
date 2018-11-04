# My Atom snippets

```

'.source.js':
  'console.log':
    'prefix': 'lo'
    'body': 'console.log(\'$1\', $1);'

  'jest:describe':
    'prefix': 'jest:describe'
    'body': """
      describe('$1', () => {
        it('$2', () => {
            $3
          });
        });
    """

  'jest:describe:describe':
    'prefix': 'jest:describe:describe'
    'body': """
      describe('$1', () => {

        describe('$2', () => {
          it('$3', () => {
              $4
            });
          });
        });
    """

  'jest:snap':
    'prefix': 'jest:snap'
    'body': """
      import React from 'react';
      import renderer from 'react-test-renderer';
      import $1 from './$1';

      describe('<$1 />', () => {
        it('renders correctly', () => {
          const props = {$2};
          const tree = renderer.create(<$1 {...props} />);
          expect(tree.toJSON()).toMatchSnapshot();
        });
      });
    """

  'jest:shallowsnap':
    'prefix': 'jest:shallowsnap'
    'body': """
      import React from 'react';
      import ShallowRenderer from 'react-test-renderer/shallow';
      import $1 from './$1';

      describe('<$1 />', () => {
        it('renders correctly', () => {
          const props = {$2};
          const renderer = new ShallowRenderer();
          renderer.render(<$1 {...props} />);
          expect(renderer.getRenderOutput()).toMatchSnapshot();
        });
      });
    """

  'rn:purecomponent':
    'prefix': 'rn:purecomponent'
    'body': """
      // @flow

      import React, { PureComponent } from 'react';
      import { View, StyleSheet } from 'react-native';

      type PropsType = {$2};

      class $1 extends PureComponent<PropsType> {

        render() {

          return (
            <View>
            </View>
          );
        }
      }

      const styles = StyleSheet.create({});

      export default $1;
    """

  'index:export':
    'prefix': 'index:export'
    'body': """
      // @flow

      export { default as $1 } from './$1';
    """

```

# My Atom plugins

- autocomplete-js-import
