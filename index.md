## Welcome to Daniel  Pages
Hi, I’m @Dimandare *My Real Name Daniel Dimas Indarputra

*I’m interested in 
* Java Development
*  Website Development(PHP,HTML,CSS)

 I’m currently learning Python Programming

NOW,
 I’m looking to collaborate on Python next project


### Markdown

This Is my latest Python project
from My team
Daniel Dimas Indarputra (V3420024),
Ammar Jadid Habibulah (V3420010),
Bagas Pratama (V342009)

```markdown
Syntax highlighted code block

 def tampilTransaksi(self):
        query = QSqlQuery("SELECT a.nik, a.nama, a.gender, t.* FROM anggota a, transaksi t WHERE a.nik=t.nik AND t.id_jenis=4")
        self.model.setQuery(query)
        self.model.setEditStrategy(QSqlTableModel.OnFieldChange)
        self.model.select()
        self.model.setHeaderData(0, Qt.Horizontal, "Kode Anggota")
        self.model.setHeaderData(1, Qt.Horizontal, "Nama")
        self.model.setHeaderData(2, Qt.Horizontal, "Jenis Kelamin")
        self.model.setHeaderData(6, Qt.Horizontal, "Jumlah Penarikan")
        self.model.setHeaderData(7, Qt.Horizontal, "Tanggal Penarikan")
        self.tableView.setModel(self.model)

        self.tableView.setColumnHidden(3,True)
        self.tableView.setColumnHidden(4,True)
        self.tableView.setColumnHidden(5,True)
        self.tableView.setColumnWidth(0, 150)
        self.tableView.setColumnWidth(1, 170)

    def simpanPenarikan(self):
        nik = self.nik.text()
        jumlah = self.jumlah.text()
        tanggal = self.tanggal.text().replace('/','-')
        if nik == "" or jumlah == "" or tanggal == "":
            self.notif.setText('Masukkan data dengan benar !')
        elif len(nik) != 16:
            self.notif.setText('Nik tidak benar !')
        else:
            self.notif.setText('')
            query = QSqlQuery()
            query.exec_("select nik from simpanan where nik='" + nik + "'")
            if query.next():
                query.exec_("insert into transaksi values(null,'" + nik + "','4','" + jumlah + "','" + tanggal + "')")
                query.exec_("select jumlah from simpanan where nik='" + nik + "'")
                if query.next():
                    hasil = query.record().value(0)
                    hasil -= int(jumlah)
                    if hasil < 0:
                        self.message.setText(" ** Penarikan melebihi jumlah simpanan **")
                        self.message.exec_()
                    else:
                        query.exec_("update simpanan set jumlah='" + str(hasil) + "' where nik='" + nik + "'")
                        self.message.setText(" ** Data berhasil ditambahkan ke database **")
                        self.message.exec_()
                        self.tampilTransaksi()
                        self.clear()
                        self.main.dfsimpan.tampilSimpanan()
            else:
                self.message.setText(" ** Anggota belum pernah menyimpan **")
                self.message.exec_()
[Link](url) and ![Image](src)
```

For more details about me see [My Profile](https://github.com/Dimandare).
For more code detail [code](https://github.com/Dimandare/Daniel).




### Support or Contact

How To reach me?
here 
Instagram : @Xeviar.co 
Github : @Dimandare

