# Workshop: Creating a Simple Chess AI with PyTorch - Introduction to neural network

## Workshop Objective

This workshop will guide you through creating a simplified chess AI using Python and PyTorch. While the AI won't be competitive, it will provide you with a basic understanding of the development process for a chess AI.

## Prerequisites

# INSTALL PYTORCH BEFORE THE WORKSHOP IT TAKES HELLA TIME
- Basic knowledge of Python.
- Python and PyTorch installed.
- [python-chess](https://python-chess.readthedocs.io/en/latest/) for chess game manipulation.

## Workshop Duration

This workshop is designed to last approximately 2.30 hours.

## Contents

## Workshop Structure
# Workshop: Creating a Simple Chess AI with PyTorch

## Workshop Objective

Welcome to the "Creating a Simple Chess AI with PyTorch" workshop. Our objective is to guide you through the process of building a basic chess AI using Python and PyTorch. While our AI may not rival grandmaster-level play, this workshop will provide you with a fundamental understanding of the key components involved in developing a chess AI.

## Prerequisites

Before we dive into this workshop, here are the prerequisites:

- **Basic Python Knowledge:** You should have a foundational understanding of the Python programming language.

- **Python and PyTorch Installed:** Make sure you have Python and PyTorch installed on your system. If not, you can find installation instructions and links below.

- **python-chess Library:** We'll use the [python-chess library](https://python-chess.readthedocs.io/en/latest/) for chess game manipulation. Ensure you have it installed.

## Workshop Duration

This workshop is designed to last approximately 2.5 hours. Here's a breakdown of what we'll cover in that time:

## Workshop Structure

### Step 1: Data Collection (15 minutes)

In this initial step, we will gather the data needed for training our chess AI. While collecting authentic chess data can be complex, we'll simplify it by generating random chess games.

```
import random
import chess

board = chess.Board()

for _ in range(10):
    legal_moves = list(board.legal_moves)
    random_move = random.choice(legal_moves)
    board.push(random_move)
    print(board)
```

The dataset will consist of board states before and after each move, allowing our AI to learn patterns.

### Step 2: Creating the Deep Learning Model (15 minutes)

The core of our chess AI is the neural network model. We'll build a simple neural network using PyTorch.

Our neural network model will serve as the brain of our chess AI. It will take a chessboard state as input and output a predicted move. The model will consist of input layers, hidden layers, and an output layer, each with its role.

```
import torch
import torch.nn as nn

class ChessAI(nn.Module):
    def __init__(self):
        super(ChessAI, self).__init()

chess_model = ChessAI()

```

While professional chess engines use highly complex models, our goal is to introduce the fundamentals of using neural networks for chess AI.

### Step 3: Model Training (1 hour)

With the model in place, it's time to train it to make intelligent moves in a chess game. Real training requires vast datasets, but for this workshop, we will use randomly generated data.


```
import random
import torch.optim as optim

criterion = nn.MSELoss()
optimizer = optim.SGD(chess_model.parameters(), lr=0.01)

for epoch in range(100):
    input_data = torch.rand(10, 64)
    target_data = torch.rand(10, 64)

    optimizer.zero_grad()

    outputs = chess_model(input_data)

    loss = criterion(outputs, target_data)
    loss.backward()
    optimizer.step()
```

Professional AI engines often undergo extensive training on powerful hardware over extended periods to achieve their remarkable skills.

### Step 4: Implementing a Simple Chess Engine (15 minutes)

Now that we've trained our model, let's create a function that allows us to play chess against the AI.

```
def play_chess_ai(ai_model, current_board):
```

Our AI will make moves without advanced chess strategies or tactics, but it is a neural network.

### Step 5: Game Visualization (15 minutes)

Finally, we will use the python-chess library to visualize the chess game.

```
import chess.svg

board = chess.Board()

board.push_san("e4")
board.push_san("e5")

board_svg = chess.svg.board(board=board)
```

Note that professional chess engines employ highly advanced visualization techniques, but our goal here is to introduce the basics.

## Required Libraries

In this workshop, you will need to install a few libraries to work with Python, PyTorch, and chess game manipulation. Below are the links and installation commands for each library:

### 1. Python

- **Link:** [Python Installation](https://www.python.org/downloads/)

   Python is the starting point for AI development, known for its simplicity and versatility.

### 2. PyTorch

- **Link:** [PyTorch Installation](https://pytorch.org/get-started/locally/)

   PyTorch is a deep learning framework that we will use for building and training the chess AI. To install PyTorch, use the provided link to access installation instructions. The installation command will depend on your system configuration. If you are using pip for Python package management, the installation command may look like this:

```   pip install torch    ```


## 3. python-chess

 ```pip install python-chess```

We will use the python-chess library for manipulating chess games in Python. To install python-chess, open your terminal or command prompt and run the provided installation command. This will download and install the library in your Python environment.

- **Link:** [PythonChess Installation](https://python-chess.readthedocs.io/en/latest/)

## 4. pandas (Data Manipulation and Analysis)

- **Link:** [pandas Installation](https://pandas.pydata.org/)

The pandas library is a versatile tool for data manipulation and analysis. We will use it for this workshop, here's the command:

```
pip install pandas
```

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Workshop by Amaury Bariety & Pierre-Louis Leroy
