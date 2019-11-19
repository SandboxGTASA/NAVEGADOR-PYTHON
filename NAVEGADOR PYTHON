

from PyQt5.QtWidgets import QApplication, QMainWindow, QToolButton, QLineEdit, QMessageBox
from PyQt5.QtWebEngineWidgets import QWebEngineView
from PyQt5.QtCore import QUrl, QSize
from PyQt5.QtGui import QIcon, QPixmap


# CARACTERISTICAS DA JANELA(ROOT)
application = QApplication([])
root = QMainWindow()
# (pos(x,y) largura(x),altura(y))
largura = 1680
altura = 1050
root.setGeometry(0, 0, largura, altura)
root.setWindowTitle('Navegador Python')
root.setMinimumHeight(altura)
root.setMaximumHeight(altura)
root.setMinimumWidth(largura)
root.setMaximumWidth(largura)
root.setStyleSheet('background-color: rgb(0,0,0);')

# WEB
home_url = 'https://www.google.com'
facebook_url = 'https://www.facebook.com'
ytb = 'https://www.youtube.com'

web = QWebEngineView(root)
web.setGeometry(0, 30, largura, altura)
web.setStyleSheet('background-color: rgb(255,255,255);')
web.load(QUrl(home_url))


# SEARCH LINE EDIT

go_line = QLineEdit(root)
go_line.setGeometry(200, 3, 255, 24)
go_line.setStyleSheet('background-color: rgb(255,255,255);')

#	BOTOES


class BT():
    def __init__(self, pos_x, png):
        self = QToolButton(root)
        self.setGeometry(pos_x, 0, 30, 30)
        self._icon = QIcon()
        self._icon.addPixmap(QPixmap(png))
        self.setIcon(self._icon)
        self.setStyleSheet('background-color: transparent;')
 ### COMO TORNAR ISSO POSSIVEL ????????????????####################################################
       "'self.clicked.connect(self.BT.ATALHOS('https://www.facebook.com'))'" ##AttributeError: 'QToolButton' object has no attribute 'BT'
        ####################################################

    def SIZEFIX(self):
        self.setIconSize(QSize(30, 30))  # fix facebook icon

    def ATALHOS(self,url):
        web.load(QUrl(url))
    	
        


home = BT(0, 'home.png')
reload = BT(40, 'reload.png')
back = BT(80, 'back.png')
forward = BT(100, 'forward.png')
search = BT(460, 'go.png')
facebook = BT(660, 'facebook.png')
twiter = BT(700, 'twiter.png')
ytb = BT(740, 'ytb.png')

# reload_bt = QToolButton(root)
# reload_bt.setGeometry(50,0,30,30)
# reload_bt_icon = QIcon()
# reload_bt_icon.addPixmap(QPixmap('reload.png'))
# reload_bt.setIcon(reload_bt_icon)
# reload_bt.setStyleSheet('background-color: transparent;')

# FUNÇOES


root.show()
application.exec_()
