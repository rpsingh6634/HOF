Question--  Higher Order Fuction (HOF) =>


Answer--
        Higher-Order Functions (HOFs) are the JavaScript functions that provide additional functionalities to the existing React component. These functions always take input values and provide return values according to the input data. That means, if the input values are changed, then the HOFs are re-run to provide the resultant return value based on the input values.

Example--
         MyHOC is a HOF which is used to pass the data to MyComponent. The function that we have created, then takes MyComponent and strengthens it with the data “newlyProvidedData” - returns the modified component which will, in turn, be rendered on to the browser.


        import React from 'react';
        var newData = {
        data: 'Data from HOC...',
        }
        var MyHOC = ComposedComponent => class extends React.Component {
        componentDidMount() {
        this.setState({
        data: newlyProvidedData.data
        });
        }
        render() {
        return ?ComposedComponent {...this.props} {...this.state} />;
        }
        };
        class MyComponent extends React.Component {
        render() {
        return (
        ? div >
        ? h1 >{this.props.data}? /h1 >
        ? /div >
        )
        }
        }
        export default MyHigherOrderFunction(MyComponent);