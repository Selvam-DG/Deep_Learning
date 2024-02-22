# Recurrent Neural Network

- A recurrent neural network (RNN) is a class of artificial neural networks where connections between nodes form a directed graph along a sequence. This allows it to exhibit temporal dynamic behavior for a time sequence.
- Unlike feedforward neural networks, RNNs can use their internal state (memory) to process sequences of inputs. This makes them applicable to tasks such as unsegmented, connected handwriting recognition or speech recognition.
- Recurrent Neural Networks produce predictive results in sequential data that other algorithms can’t
- But when do you need to use a Recurrent Neural Network?
  - “Whenever there is a sequence of data and that temporal dynamics that connects the data is more important than the spatial content of each individual frame.”– Lex Fridman (MIT)
- Output = Activation_function ( memory + (weights*features) )
  - for example , y = tanh( (Wy*Yt-1) + (Wx * Xi))
  -
![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/041a266e-ddf4-44c1-acf1-8b028a316917)



![Screenshot 2024-02-22 170315](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/d2a58560-2bd9-4e39-9958-474043ee6a88)


- Vanishing gradient -
  - In deep Neural Networks the differential of activation function such as sigmoid and Tanh gives extremely small values and it fails to change the weights substantially.
  - It stops getting context carried through a large number of words/inputs in a sequence mode
- Exploding gradient- using the Relu function
- RNN has the drawback of short memory
#### LSTM (Long Short term memory)

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/f68c5cc0-e90f-4961-8384-4f23988a8375)
![images](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/6e1bd491-27b8-44ec-8fbb-68f549f2a204)

- 
- Long Short-Term  Memory Networks – usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies. They were introduced by Hochreiter & Schmidhuber (1997)
- LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering information for long periods of time is practically their default behavior, not something they struggle to learn
 ![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/07fef535-2874-4e98-9b87-213018f5b9f8)
- Input layer => Hidden Layer ( LSTM layer ) => Output layer
- Individual input layer is connected to LSTM hidden layers which are not fully connected to the input layer and do perform computation by applying activation function, result the output
- RNN is time-based prediction
- In RNN, we use Sigmoid and tanh
- A Special Kind of RNN
- 
- 
![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/982700e5-4157-4268-8b91-45454a2c0c4b)

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/f65da803-abdd-43ce-b703-650d71bcfb88)

- Gate
  -  The sigmoid layer outputs numbers between zero and one, describing how much of each component should be let through. A value of zero means “let nothing through,” while a value of one means “let everything through!”

- Input gate (it)
- Forget gate (ft)
- Output gate ((Ot)
- Ct is Long term memory
- ht is short-term memory
- The input gate defines how much of the newly computed state for the current input you want to let through.
- The forget gate defines how much of the previous state you want to let through.
- The output gate defines how much of the internal state you want to expose to the external network (higher layers and the next time step). All the gates have the same dimensions ds, the size of your hidden state.

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/d0cdc0e8-39c8-450f-bd79-074594c67af4)



#### GRU (Gated Recurrent Unit)
-  A GRU has two gates, a reset gate r, and an update gate z.  Intuitively, the reset gate determines how to combine the new input with the previous memory, and the update gate defines how much of the previous memory to keep around. 
- If we set the reset to all 1’s and  update gate to all 0’s we arrive at plain RNN model
-  A GRU has two gates, an LSTM has three gates.
-  We don’t apply a second nonlinearity when computing the output. (like tanh in LSTM at last output)

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/60124834-294e-4511-ad24-1445542a3e14)






