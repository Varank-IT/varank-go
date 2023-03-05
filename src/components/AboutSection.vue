<template>
    <section class="bio-section">
        <div id="bio">
            <SectionLabel label="Etkinlik Hakkında" />
            <p>
                VarankGO; Şehit İlhan Varank Fen Lisesi’nde liseli gençlerin katılımıyla, 28-29-30 Nisan 2023
                tarihlerinde gerçekleştirilecek bir inovasyon kampıdır. Bu sene üçüncüsünü düzenlediğimiz
                etkinliğimizde; katılımcılar çeşitli şirketlerin ortaya sunduğu case’lere ekip arkadaşlarıyla birlikte
                rasyonel ve yenilikçi çözümler getirecek, bunun beraberinde çeşitli ilgi alanlarına hitap eden
                workshoplara katılım sağlayıp donanımlı konuşmacılarımızı dinleme fırsatı yakalayacak.
            </p>
            <h2 class="sub-h">Amaçlarımız</h2>
            <p>
                VarankGO’nun amacı, katılımcılarımızı kurumsal hayata hazırlarken onlara hayat tecrübesi kazandırmak,
                21. yüzyılın iş dünyasında aranan nitelikleri katılımcılara aşılamak ve başarıyla takım çalışması
                yapabilme, sunum yapma,inovatif çözümler üretme, çevre okullardan insanlarla kaynaşarak çevrenizi
                büyütme ve topluluk/takım içerisinde fikirlerini rahatça beyan edebilme gibi beceriler kazandırmaktır.
                Kendilerini birçok farklı yönden geliştirmenin yanı sıra çeşitli workshoplarımız ve etkinliklerimizle bu
                tecrübeyi eğlenceli kılmaktır.

            </p>
            <h2 class="sub-h">Misyonumuz</h2>
            <p>
                Çevre okullarla iletişimimizi/bağlarımızı kuvvetlendirmek, katılımcı arkadaşlarımıza unutulmaz bir
                deneyim yaşatmak ve farklı bir deneyim aşılamak, katılımcıların kendi arasındaki iletişim becerilerini
                kuvvetlendirerek kendilerini ifade edebilme becerilerini daha üst bir seviyeye çıkarmak, takım
                içerisinde dayanışmayı arttırmak, workshoplarımız aracılığıyla farklı ilgi alanlarıyla ilgilenebilme
                fırsatı yakalayabilmek ve en önemlisi katılımcılarımızın memnuniyetini en üst seviyede tutabilmek,
                etkinliğimizde bulunan bütün arkadaşlarımızın eğlenceli,keyifli ve değerli zaman geçirmelerini sağlamak
                bizim görevimizdir.
            </p>
            <h2 class="sub-h">Vizyonumuz</h2>
            <p>
                Lise dönemindeki gençlerimizi iş dünyasında uzmanlaşmış kişilerle buluşturarak toplumumuza kriz
                yönetimi, iletişim, problem çözme, yenilikçi düşünme becerisi yüksek, kendini ifade edebilme yetenekleri
                gelişmiş bireyler kazandırmak.
            </p>
        </div>
    </section>
</template>

<script>
import SectionLabel from './SectionLabel.vue'

export default {
    name: 'AboutSection',
    components: {
        SectionLabel
    }
}
</script>

<style scoped>
#bio {
    font-size: 20px;
    margin-left: 12%;
    margin-right: 12%;
    margin-top: 50px;
    word-spacing: normal;
    text-align: center;
}

.sub-h {
    font-size: 30px;
}
</style>
