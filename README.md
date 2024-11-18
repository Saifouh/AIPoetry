
# Shakespeare LSTM Text Generator  
A character-level text generation model that uses LSTM to generate Shakespearean-style text. This project demonstrates how deep learning can be applied to sequence modeling tasks like text generation.  

## Features  
- **Character-Level Text Generation**: The model learns and predicts text at the character level.  
- **Adjustable Creativity**: Control the creativity of generated text using a `temperature` parameter.  
- **Pre-Trained Model**: A saved model is included for generating text immediately.  

## Prerequisites  
- Python 3.x  
- TensorFlow >= 2.0  
- NumPy  

## Setup  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/Shakespeare-LSTM-Text-Generator.git
   cd Shakespeare-LSTM-Text-Generator
   ```
2. Install dependencies:  
   ```bash
   pip install tensorflow numpy
   ```

## Usage  

### First Run: Train the Model  
**Note:** Ensure comments around the training block are removed before running the script for the first time. This will train the model and save it for future use.  
```python
# Uncomment this block for the first run:
# model = Sequential()
# model.add(LSTM(128, input_shape=(SEQ_LENGTH, len(characters))))
# model.add(Dense(len(characters)))
# model.add(Activation('softmax'))
#
# model.compile(loss='categorical_crossentropy', optimizer=RMSprop(learning_rate=0.01))
#
# model.fit(x, y, batch_size=256, epochs=4)
# model.save('textgenerator.h5')
```
Run the script to train the model:  
```bash
python text_generator.py
```

### Generate Text with Pre-Trained Model  
Once the model is saved (`textgenerator.h5`), the training block can remain commented. Directly use the model to generate text:  
```bash
python text_generator.py
```

You will see generated text with varying creativity levels:  
```plaintext
---------0.2------------
<Generated text with low creativity>
---------0.4------------
<Generated text with moderate creativity>
---------0.6------------
<Generated text with balanced creativity>
---------0.8------------
<Generated text with higher creativity>
---------1.0------------
<Generated text with maximum creativity>
```

## Adjustable Creativity  
Use the `temperature` parameter to control the creativity of generated text.  
- Low temperature (e.g., 0.2): Predictable, repetitive text.  
- High temperature (e.g., 1.0): Diverse, creative text with possible errors.  

## Example Output  
Sample text generated at different temperatures:  
```plaintext
Temperature: 0.2  
"the king and the king the king the king and the king and the king and the king and the king"  

Temperature: 0.6  
"the king and the duke of a friend of the world and the king that we have a man shall see"  

Temperature: 1.0  
"the king hath flove thee blonder love; the greateful doth witherful'd to me all this heaven."  
```

## Contributing  
Contributions are welcome! If you'd like to improve this project, feel free to fork the repository and submit a pull request.

## License  
This project is licensed under the MIT License.  

---

Happy text generating! 🎭
