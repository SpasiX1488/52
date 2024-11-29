# 52
from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QLabel, QVBoxLayout
from instr import*
from second_win import*
from final_win import*
from second_win.py import*

class MainWin(QWidget):
    def __init__(self):
        super().__init__()
        self.set_appear()
        self.initUI()
        self.connects()
        self.show()
    def set_appear(self):
        self.setWindowTitle(txt_title)
        self.resize(win_width, win_height)
        self.move(win_x, win_y)
    def initUI(self):
        self.hello_text = QLabel(txt_hello)
        self.instruction = QLabel(txt_instruction)
        self.btn_next = QPushButton(txt_next)
        self.layout = QVBoxLayout()
        self.layout.addWidget(self.hello_text, alignment = Qt.AlignLeft)
        self.layout.addWidget(self.instruction, alignment = Qt.AlignLeft)
        self.layout.addWidget(self.btn_next, alignment = Qt.AlignCenter)
        self.setLayout(self.layout)
    def next_click(self):
        self.tw = TestWin()
        self.hide()
    def connects(self):
        self.btn_next.clicked.connect(self.next_click)

app = QApplication([])
mw = MainWin()
app.exec_()




from PyQt5.QtCore import *
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QLabel, QVBoxLayout, QLineEdit
from instr import *
from my_app.py import*

class TestWin(Qwidget):

    def __init__(self):
        super.__init__()
        self.set_appear()
        self.initUI()
        self.connects()
        self.show()

    def initUI(self):
        self.btn_next = QPushButton(txt_sendresults, self)
        self.btn_test1 = QPushButton(txt_starttest1, self)
        self.btn_test2 = QPushButton(txt_starttest2, self)
        self.btn_test3 = QPushButton(txt_starttest3, self)

        self.text_name = QLabel(txt_name)
        self.text_age = QLabel(txt_age)
        self.text_test1 = QLabel(txt_test1)
        self.text_test2 = QLabel(txt_test2)
        self.text_test3 = QLabel(txt_test3)
        self.text_timer = QLabel(txt_timer)

        self.line_name = QLineEdit(txt_hintname)
        self.line_age = QLineEdit(txt_hinage)
        self.line_test1 = QLineEdit(txt_hintest1)
        self.line_test2 = QLineEdit(txt_hintest2)
        self.line_test3 = QLineEdit(txt_hintest3)

        self.h_line = QVBoxLayout()
        self.r_line = QVBoxLayout()
        self.l_line = QVBoxLayout()

        self.r_line.addWidget(self.test_timer, alignment = Qt.AlignCenter)

        self.r_line.addWidget(self.text_name, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.line_name, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.text_age, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.line_age, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.text_test1, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.btn_test1, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.line_test1, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.text_test2, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.btn_test2, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.text_test3, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.btn_test3, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.line_test2, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.line_test3, alignment = Qt.AlignLeft)
        self.r_line.addWidget(self.btn_next, alignment = Qt.AlignCenter)

        self.h_line.addLayout(self.l_line)
        self.h_line.addLayout(self.r_line)

        self.setLayout(self.h_line)

    def next_click(self):
        self.hide()
        self.fw = FinalWin()
        
    def connects(self):
        self.btn_next.clicked.connect(self.next_click)

    def set_appear(self):
            self.setWindowTitle(txt_title)
            self.resize(win_width, win_height)
            self.move(win_x, win_y)


            from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import QApplication, QWidget, QPushButton, QLabel, QVBoxLayout
from instr import*


class Finalnwin(QWidget):
    def __init__(self):
        super().__init__()
        self.initUi()
        self.set_appear()
        self.show()
    def initUi(self):
        self.label = QLabel('лоплоапло')
        self.label2 = QLabel('lgflgflg')
        self.line = QVBoxLayout()
        self.line.addWidget(self.label)
        self.line.addWidget(self.label2)
        self.setLayout(self.line)



        
    def set_appear(self):
        self.setWindowTitle(txt_title)
        self.resize(win_width, win_height)
        self.move(win_x, win_y)
    
