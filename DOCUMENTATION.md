<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [Group][1]
    -   [Parameters][2]
-   [Layer][3]
    -   [Parameters][4]
-   [Neuron][5]
    -   [Parameters][6]
    -   [Neuron#project][7]
        -   [Parameters][8]
    -   [Neuron#is][9]
    -   [Neuron#is.input][10]
    -   [Neuron#is.ouput][11]
    -   [Neuron#activate][12]
        -   [Parameters][13]
    -   [Neuron#propagate][14]
        -   [Parameters][15]
    -   [Neuron.activations][16]
    -   [Neuron.activations.SIGMOID][17]
        -   [Parameters][18]
    -   [Neuron.activations.RELU][19]
        -   [Parameters][20]
    -   [Neuron.activations.TANH][21]
        -   [Parameters][22]
    -   [Neuron.activations.LINEAR][23]
        -   [Parameters][24]
-   [propagate][25]
    -   [Parameters][26]
-   [project][27]
    -   [Parameters][28]

## Group

Represents a Group of Neurons.

### Parameters

-   `props`  
-   `options` **[array][29]** 

## Layer

Represents a Layer of Neurons.

### Parameters

-   `props` **[object][30]** 
-   `options` **[array][29]** 

## Neuron

> Neuron Factory Function

-   CHECK: [https://robertbeisicht.wordpress.com/2014/07/04/feed-forward-neural-network-in-javascript/][31]
-   CHECK: [https://medium.com/javascript-scene/javascript-factory-functions-with-es6-4d224591a8b1][32]
-   CHECK: [https://softwareengineering.stackexchange.com/questions/82593/javascript-ternary-operator-vs][33]

### Parameters

-   `props` **[Object][30]?** Neuron's Properties
    -   `props.bias` **[number][34]** Neuron's Synaptic Weight Constant AKA Bias (optional, default `Math.random()`)
    -   `props.activation` **ActivationFunction** Neuron's Activation Function (optional, default `Neuron.activations.SIGMOID`)
    -   `props.rate` **[number][34]** Neuron's Learning Rate AKA Gradient Descent Step Size (optional, default `0.3`)
    -   `props.connections` **[Object][30]?** Neuron's Connections
        -   `props.connections.incoming` **\[Connection]** Neuron's Incoming Connections (optional, default `[]`)
        -   `props.connections.outgoing` **\[Connection]** Neuron's Outgoing Connections (optional, default `[]`)

### Neuron#project

Projects this neuron to given neuron.

#### Parameters

-   `neuron` **[Neuron][35]** Destination `neuron`
-   `weight` **[number][34]?** Connection `weight`
-   `callback` **ConnectionCallback?** Callback invoked with _(error, connection)_

### Neuron#is

### Neuron#is.input

Returns **[boolean][36]** Returns `true` if this neuron has no incoming connections

### Neuron#is.ouput

Returns **[boolean][36]** Returns `true` if this neuron has no outgoing connections

### Neuron#activate

Activates this neuron and returns squashed results

#### Parameters

-   `input` **[number][34]?** Real number (-∞, ∞)
-   `callback` **NumberCallback?** Callback invoked with _(error, result)_

### Neuron#propagate

Updates this neurons weight and returns error

#### Parameters

-   `feedback` **[number][34]?** Real number (-∞, ∞)
-   `callback` **NumberCallback?** Callback invoked with _(error, result)_

### Neuron.activations

### Neuron.activations.SIGMOID

#### Parameters

-   `x` **[number][34]** Real Number Input
-   `derivative` **[boolean][36]** Return partial derivative

### Neuron.activations.RELU

#### Parameters

-   `x` **[number][34]** Real Number Input
-   `derivative` **[boolean][36]** Return partial derivative

### Neuron.activations.TANH

#### Parameters

-   `x` **[number][34]** Real Number Input
-   `derivative` **[boolean][36]** Return partial derivative

### Neuron.activations.LINEAR

#### Parameters

-   `x` **[number][34]** Real Number Input
-   `derivative` **[boolean][36]** Return partial derivative

## 

[x] Case "Input Neuron": Forward Input; Return Input
[x] Case "Hiddent/Output Neuron": Sum Inputs; Squash Sum; Store Squashed Sum; Return Squashed Sum

## propagate

Assumes `feedback` is the Net Error with respect to this neuron

[ ] Learn How to Cleanly Set This Up
[ ] Case "Output Neuron": Multiply `feedback` by Activation Derivative; Return Chained Expression
[ ] Case "Hidden/Input": Sum Net Errrors; Multiply Net Error by Activation Derivative; Update Weights; Return Chained Expression

### Parameters

-   `feedback`  
-   `callback`  

## project

[x] Create a new Connection
[x] Add Connection to both Neurons
[x] Return Connection

### Parameters

-   `neuron`  
-   `weight`  
-   `callback`  

[1]: #group

[2]: #parameters

[3]: #layer

[4]: #parameters-1

[5]: #neuron

[6]: #parameters-2

[7]: #neuronproject

[8]: #parameters-3

[9]: #neuronis

[10]: #neuronisinput

[11]: #neuronisouput

[12]: #neuronactivate

[13]: #parameters-4

[14]: #neuronpropagate

[15]: #parameters-5

[16]: #neuronactivations

[17]: #neuronactivationssigmoid

[18]: #parameters-6

[19]: #neuronactivationsrelu

[20]: #parameters-7

[21]: #neuronactivationstanh

[22]: #parameters-8

[23]: #neuronactivationslinear

[24]: #parameters-9

[25]: #propagate

[26]: #parameters-10

[27]: #project

[28]: #parameters-11

[29]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[30]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[31]: https://robertbeisicht.wordpress.com/2014/07/04/feed-forward-neural-network-in-javascript/

[32]: https://medium.com/javascript-scene/javascript-factory-functions-with-es6-4d224591a8b1

[33]: https://softwareengineering.stackexchange.com/questions/82593/javascript-ternary-operator-vs

[34]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[35]: #neuron

[36]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean