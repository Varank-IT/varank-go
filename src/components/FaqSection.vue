<template>
    <section class="faq-section">
        <div class="faq-warp">
            <div class="container">
                <SectionLabel label="Sıkça Sorulan Sorular" />
                <div class="row">
                    <div class="faq">
                        <AccordionItem v-for="(faq, index) in faqs" :key="faq" :info="faq" :badgeNumber="index + 1" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Badge from './accordion/Badge.vue';
import SectionLabel from './SectionLabel.vue'
import AccordionItem from './accordion/AccordionItem.vue';

export default {
    name: 'FaqSection',
    components: {
        Badge,
        SectionLabel,
        AccordionItem
    },
    data: () => ({
        faqs: [
            {
                question: 'Etkinliğin tarihi nedir?',
                answer: 'Etkinliğimiz 28-29-30 Nisan tarihlerinde üç gün içinde gerçekleştirilecektir.'
            },
            {
                question: 'Case/Case sponsorluğu ne anlama geliyor?',
                answer: 'Case; bir şirketin sunduğu, katılımcıların çözmek için pek çok farklı fikir ortaya koyabileceği problemdir. Case sponsoru ise case’leri katılımcılara sunacak şirkettir.'
            },
            {
                question: 'Workshop nedir?',
                answer: 'Workshop sözcük olarak atölye anlamına gelir. Aklınızı çalıştırırken bir yandan da dinlenmenizi sağlayacak birtakım etkinliklerdir. '
            },
            {
                question: 'Etkinlik sonunda sertifika verilecek mi?',
                answer: 'Evet, sertifika veriyoruz.'
            },
            {
                question: 'Etkinliğe kimler katılabiliyor?',
                answer: 'İstanbul genelindeki bütün hazırlık, 9, 10, 11 ve 12. sınıf öğrencileri 5-6 kişilik ekiplerle katılım sağlayabilir.'
            },
            {
                question: 'Etkinlik ücreti nedir?',
                answer: 'Etkinlik ücreti kısa zaman içinde duyurulacaktır.'
            },
            {
                question: 'Dresscode var mı?',
                answer: 'İlk iki gün smart casual son gün formal olacak.'
            }
        ]
    })
}
</script>

<style scoped>
.faq-section {
    min-height: 100vh;
    min-height: 50vh;
    font-weight: bold;
    text-align: left;
}

.faq-warp {
    /*padding: 6vh 4vw;*/
    padding: 2vh 12vw;
}

.faq {
    background: #FFFFFF;
    box-shadow: 0 2px 48px 0 rgba(0, 0, 0, 0.06);
    border-radius: 4px;
}

@media (max-width: 1000px) {
    .faq {
        margin-bottom: 30px;
    }
}
</style>