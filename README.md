from flask import Flask
import random

app = Flask(__name__)



ilginc_bilgiler = [
    "Teknolojik bağımlılıktan mustarip olan çoğu kişi, kendilerini şebeke kapsama alanı dışında bulduklarında veya cihazlarını kullanamadıkları zaman yoğun stres yaşarlar.",
    "2018 yılında yapılan bir araştırmaya göre 18-34 yaş arası kişilerin %50'den fazlası kendilerini akıllı telefonlarına bağımlı olarak görüyor.",
    "Teknolojik bağımlılık çalışması, modern bilimsel araştırmanın en ilgili alanlarından biridir.",
    "2019'da yapılan bir araştırmaya göre, insanların %60'ından fazlası akıllı telefonlarındaki iş mesajlarına işten ayrıldıktan sonraki 15 dakika içinde yanıt veriyor.",
    "Teknolojik bağımlılıkla mücadele etmenin bir yolu, zevk veren ve ruh halini iyileştiren faaliyetler aramaktır.",
    "Elon Musk, sosyal ağların içeriği görüntülemek için mümkün olduğunca fazla zaman harcamamız için bizi platformun içinde tutmak üzere tasarlandığını iddia ediyor."
    ]

sifre_olusturucu = [
    "1.L7p@8Fg5r9Zq#1W*",
    "2.Qz1^Tg#4lVb8Mp*",
    "3.Rw9#r3Hv!2K7@yJ",
    "4.Jk!4Pf6&z0Tc@5B",
    "5.Mt#7Xy$3xCq!9Gh",
    "6.Vd8Qz2^k9Lp@4R*",
    "7.Wf6@Yh4l7N3#Bv*",
    "8.Xy!5Bp2$r8Qk#1W",
    "9.Bq7$Jr3^n1Kv@2Z",
    "10.Nf7$k!3Ze#6Pq@G"
]


@app.route("/")
def hello_world():
    return f'<p>Hoş Geldiniz </p><a href="/ilginc-bilgiler">İlginç Bilgiler</a>'

@app.route("/")
def selam():
    return f'<p>Hoş Geldiniz </p><a href="/sifre_olusturucu">Sifre_olusturucu</a>'

@app.route("/ilginc-bilgiler")
def rafiq():
    return f"<p>İlginç Bilgiler: {random.choice(ilginc_bilgiler)}</p>"

@app.route("/sifre_olusturucu")
def sifre():
    return f"<p>Şifre_olusturucu: {random.choice(sifre_olusturucu)}</p>"

app.run(debug=True)
