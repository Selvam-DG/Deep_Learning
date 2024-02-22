# Recurrent Neural Network

- A recurrent neural network (RNN) is a class of artificial neural networks where connections between nodes form a directed graph along a sequence. This allows it to exhibit temporal dynamic behavior for a time sequence.
- Unlike feedforward neural networks, RNNs can use their internal state (memory) to process sequences of inputs. This makes them applicable to tasks such as unsegmented, connected handwriting recognition or speech recognition.
- Recurrent Neural Networks produce predictive results in sequential data that other algorithms can’t
- But when do you need to use a Recurrent Neural Network?
  - “Whenever there is a sequence of data and that temporal dynamics that connects the data is more important than the spatial content of each individual frame.”– Lex Fridman (MIT)
- Output = Activation_function ( memory + (weights*features) )
  - for example , y = tanh( (Wy*Yt-1) + (Wx * Xi))
  -

  ![Screenshot 2024-02-22 170315](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/d2a58560-2bd9-4e39-9958-474043ee6a88)


- Vanishing gradient - 
- Exploding gradient- using Relu function
- RNN has drawback of short memory
#### LSTM (Long Short term memory)

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/f68c5cc0-e90f-4961-8384-4f23988a8375)

- 
- Long Short-Term  Memory Networks – usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies. They were introduced by Hochreiter & Schmidhuber (1997)
- LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering information for long periods of time is practically their default behavior, not something they struggle to learn
 
- Input layer => Hidden Layer ( LSTM layer ) => Output layer
- Individual input layer is connected to LSTM hidden layers which are not fully connected to the input layer and do perform computation by applying activation function, result the output
- RNN is time-based prediction
- In RNN, we use Sigmoid and tanh
- A special Kind of RNN
- 
- 
![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/982700e5-4157-4268-8b91-45454a2c0c4b)

![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/f65da803-abdd-43ce-b703-650d71bcfb88)

- Gate
  -  The sigmoid layer outputs numbers between zero and one, describing how much of each component should be let through. A value of zero means “let nothing through,” while a value of one means “let everything through!”

- Forget gate ft
- 
![download](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/d0cdc0e8-39c8-450f-bd79-074594c67af4)







