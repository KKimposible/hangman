def hangman(word):
  wrong = 0
  stages = ["", 
            "__________            ",
            "|                     ",
            "|         |           ",
            "|         0           ",
            "|      /  |  \        ",
            "|       /   \         ",
            "|                     ",
           ]
  rletters = list(word)
  board = ["_"] * len(word)
  win = False
  print("ハングマンにようこそ")
  while wrong < len(stages) - 1:
    print("/n")
    msg = "１文字を予想してね"
    char = input(msg)
    if char in rletters:
      cind = rletters.index(char)
      board[cind] = char
      rletters[cind] = '$'
    else:
      wrong += 1
    print(" ".join(board))
    e = wrong + 1
    print("\n".join(stages[0:e]))
    if "_" not in board:
      print("you are winner")
      print("_".join(board))
      win = True
      break
  if not win:
    print("\n".join(stages[0:wrong+1]))
    print("you are lose! Correct is {}.".format(word))
hangman("cat")
