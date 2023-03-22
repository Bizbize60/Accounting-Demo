# MAVI-UI-2#
#USER Interface#
from PyQt5 import QtCore, QtGui, QtWidgets
import mysql.connector

class Ui_MainWindow(object):
    def setupUi(self, MainWindow):
        MainWindow.setObjectName("MainWindow")
        MainWindow.resize(800, 600)
        self.centralwidget = QtWidgets.QWidget(MainWindow)
        self.centralwidget.setObjectName("centralwidget")
        self.tableWidget = QtWidgets.QTableWidget(self.centralwidget)
        self.tableWidget.setGeometry(QtCore.QRect(60, 0, 721, 300))
        self.tableWidget.setRowCount(50000)
        self.tableWidget.setObjectName("tableWidget")
        self.tableWidget.setColumnCount(7)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(0, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(1, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(2, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(3, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(4, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(5, item)
        item = QtWidgets.QTableWidgetItem()
        self.tableWidget.setHorizontalHeaderItem(6, item)
        self.lineEdit = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit.setGeometry(QtCore.QRect(60, 300, 133, 20))
        self.lineEdit.setObjectName("lineEdit")
        self.lineEdit_2 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_2.setGeometry(QtCore.QRect(60, 320, 133, 20))
        self.lineEdit_2.setObjectName("lineEdit_2")
        self.lineEdit_3 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_3.setGeometry(QtCore.QRect(60, 340, 133, 20))
        self.lineEdit_3.setObjectName("lineEdit_3")
        self.lineEdit_4 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_4.setGeometry(QtCore.QRect(60, 360, 133, 20))
        self.lineEdit_4.setObjectName("lineEdit_4")
        self.lineEdit_5 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_5.setGeometry(QtCore.QRect(60, 380, 133, 20))
        self.lineEdit_5.setObjectName("lineEdit_5")
        self.lineEdit_6 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_6.setGeometry(QtCore.QRect(60, 400, 133, 20))
        self.lineEdit_6.setObjectName("lineEdit_6")
        self.pushButton = QtWidgets.QPushButton(self.centralwidget,clicked=lambda:self.save())
        self.pushButton.setGeometry(QtCore.QRect(193, 300, 91, 121))
        self.pushButton.setObjectName("pushButton")
        self.label = QtWidgets.QLabel(self.centralwidget)
        self.label.setGeometry(QtCore.QRect(290, 300, 47, 20))
        self.label.setObjectName("label")
        self.label_2 = QtWidgets.QLabel(self.centralwidget)
        self.label_2.setGeometry(QtCore.QRect(290, 320, 47, 20))
        self.label_2.setObjectName("label_2")
        self.label_3 = QtWidgets.QLabel(self.centralwidget)
        self.label_3.setGeometry(QtCore.QRect(290, 340, 47, 20))
        self.label_3.setObjectName("label_3")
        self.label_4 = QtWidgets.QLabel(self.centralwidget)
        self.label_4.setGeometry(QtCore.QRect(290, 360, 47, 20))
        self.label_4.setObjectName("label_4")
        self.label_5 = QtWidgets.QLabel(self.centralwidget)
        self.label_5.setGeometry(QtCore.QRect(290, 380, 47, 20))
        self.label_5.setObjectName("label_5")
        self.label_6 = QtWidgets.QLabel(self.centralwidget)
        self.label_6.setGeometry(QtCore.QRect(290, 400, 47, 20))
        self.label_6.setObjectName("label_6")
        self.lineEdit_7 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_7.setGeometry(QtCore.QRect(330, 320, 133, 20))
        self.lineEdit_7.setObjectName("lineEdit_7")
        self.lineEdit_8 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_8.setGeometry(QtCore.QRect(330, 360, 133, 20))
        self.lineEdit_8.setObjectName("lineEdit_8")
        self.lineEdit_9 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_9.setGeometry(QtCore.QRect(330, 380, 133, 20))
        self.lineEdit_9.setObjectName("lineEdit_9")
        self.lineEdit_10 = QtWidgets.QLineEdit(self.centralwidget)
        self.lineEdit_10.setGeometry(QtCore.QRect(330, 400, 133, 20))
        self.lineEdit_10.setObjectName("lineEdit_10")
        self.pushButton_2 = QtWidgets.QPushButton(self.centralwidget,clicked=lambda:self.edit())
        self.pushButton_2.setGeometry(QtCore.QRect(460, 300, 91, 121))
        self.pushButton_2.setObjectName("pushButton_2")
        self.pushButton_3 = QtWidgets.QPushButton(self.centralwidget,clicked=lambda:self.load_data())
        self.pushButton_3.setGeometry(QtCore.QRect(660, 300, 121, 81))
        self.pushButton_3.setObjectName("pushButton_3")
        MainWindow.setCentralWidget(self.centralwidget)
        self.menubar = QtWidgets.QMenuBar(MainWindow)
        self.menubar.setGeometry(QtCore.QRect(0, 0, 800, 21))
        self.menubar.setObjectName("menubar")
        MainWindow.setMenuBar(self.menubar)
        self.statusbar = QtWidgets.QStatusBar(MainWindow)
        self.statusbar.setObjectName("statusbar")
        MainWindow.setStatusBar(self.statusbar)

        self.retranslateUi(MainWindow)
        QtCore.QMetaObject.connectSlotsByName(MainWindow)

    def retranslateUi(self, MainWindow):
        _translate = QtCore.QCoreApplication.translate
        MainWindow.setWindowTitle(_translate("MainWindow", "MainWindow"))
        item = self.tableWidget.horizontalHeaderItem(0)
        item.setText(_translate("MainWindow", "sayı"))
        item = self.tableWidget.horizontalHeaderItem(1)
        item.setText(_translate("MainWindow", "merkez"))
        item = self.tableWidget.horizontalHeaderItem(2)
        item.setText(_translate("MainWindow", "sayac no"))
        item = self.tableWidget.horizontalHeaderItem(3)
        item.setText(_translate("MainWindow", "geliş"))
        item = self.tableWidget.horizontalHeaderItem(4)
        item.setText(_translate("MainWindow", "çıkış"))
        item = self.tableWidget.horizontalHeaderItem(5)
        item.setText(_translate("MainWindow", "fiyat-geliş"))
        item = self.tableWidget.horizontalHeaderItem(6)
        item.setText(_translate("MainWindow", "fiyat-çıkış"))
        self.pushButton.setText(_translate("MainWindow", "PushButton"))
        self.label.setText(_translate("MainWindow", "MERKEZ"))
        self.label_2.setText(_translate("MainWindow", "SAYAC"))
        self.label_3.setText(_translate("MainWindow", "GELİŞ"))
        self.label_4.setText(_translate("MainWindow", "ÇIKIŞ"))
        self.label_5.setText(_translate("MainWindow", "GELİŞ-F"))
        self.label_6.setText(_translate("MainWindow", "ÇIKIŞ-F"))
        self.pushButton_2.setText(_translate("MainWindow", "PushButton"))
        self.pushButton_3.setText(_translate("MainWindow", "YENILE"))
    def save(self): 
         mydb=mysql.connector.connect(
             host="localhost",
             user="root",
             password="Tu41893982790",
             database="deneme")
         mycursor=mydb.cursor()
         sql="INSERT INTO mavi(merkez,sayac_no,gelis_tarihi,cikis_tarihi,gelis_fiyati,cikis_fiyati) VALUES(%s,%s,%s,%s,%s,%s)"
         
         val=(str(self.lineEdit.text()),str(self.lineEdit_2.text()),str(self.lineEdit_3.text()),str(self.lineEdit_4.text()),str(self.lineEdit_5.text()),str(self.lineEdit_6.text()))
         
         mycursor.execute(sql,val)
         mydb.commit()
    def edit(self): 
        mydb=mysql.connector.connect(
            host="localhost",
            user="root",
            password="Tu41893982790",
            database="deneme")
        mycursor=mydb.cursor()
        sql=f"UPDATE mavi SET cikis_tarihi={self.lineEdit_8.text()},gelis_fiyati={self.lineEdit_9.text()},cikis_fiyati={self.lineEdit_10.text()} WHERE sayac_no={self.lineEdit_7.text()}"
        mycursor.execute(sql)
        mydb.commit()     
    def load_data(self):
            mydb=mysql.connector.connect(
                host="localhost",
                user="root",
                password="Tu41893982790",
                database="deneme")
            mycursor=mydb.cursor()
            sql="SELECT * FROM mavi"
            mycursor.execute(sql)
            results=mycursor.fetchall()
            results.reverse()
            results=list(results)
            row=0
            
            for sayac in results:
                self.tableWidget.setItem(row,0,QtWidgets.QTableWidgetItem(str(sayac[0])))
                self.tableWidget.setItem(row,1,QtWidgets.QTableWidgetItem(str(sayac[1])))
                self.tableWidget.setItem(row,2,QtWidgets.QTableWidgetItem(str(sayac[2])))
                self.tableWidget.setItem(row,3,QtWidgets.QTableWidgetItem(str(sayac[3])))
                self.tableWidget.setItem(row,4,QtWidgets.QTableWidgetItem(str(sayac[4])))
                self.tableWidget.setItem(row,5,QtWidgets.QTableWidgetItem(str(sayac[5])))
                self.tableWidget.setItem(row,6,QtWidgets.QTableWidgetItem(str(sayac[6])))
               
                row+=1     

if __name__ == "__main__":
    import sys
    app = QtWidgets.QApplication(sys.argv)
    MainWindow = QtWidgets.QMainWindow()
    ui = Ui_MainWindow()
    ui.setupUi(MainWindow)
    MainWindow.show()
    sys.exit(app.exec_())

