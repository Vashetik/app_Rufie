# app_Rufie
from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import(QApplication, QWidget, QLabel, QVBoxLayout, QHBoxLayout, QMessageBox)



class MainWin(QWidget):
    def __init__(self):
        super().__init__()
        self.set_appear()
        self.initUI()
        self.connects()
        self.show()

    def set_appear(self):
        self.setWindowTitle(txt_title)
        self.resize(win_windt, win_height)
        self.move(win_x, win_y)
    
    def initUI(self):
        self.hello_text = QLabel(txt_hello)
        self.instruction = Qlabel(txt_instruction)
        self.button = QPushButton(txt_next)
        self.layout = QVBoxLayout
        self.layout.addWidget(self.hello_text)
        self.layout.addChildWidget(self.instruction)
        self.layout.addWidget(self.button)
    
    def connects(self):
        self.btn_next.clicked.connect(self.next_click)
    
    def next_click(self):
        self.hide()
        self.tw = TestWin()
