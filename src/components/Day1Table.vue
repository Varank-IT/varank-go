<template>
    <div style="overflow-x: auto;" id="schedule">
        <SectionLabel label="Organizasyon Takvimi" />
        <table>
            <tr>
                <th style="font-size: 20px;">Gün 1 (4 Mart)</th>
                <th style="font-size: 20px;">Yeditepe</th>
            </tr>
            <tr>
                <td>09.00-10.00</td>
                <td>Kayıtlar ve Kahvaltı</td>
            </tr>
            <tr>
                <td>10.00-11.00</td>
                <td>Açılış Konuşması ve Üniversite Tanıtım Videosu</td>
            </tr>
            <tr>
                <td>11.00-11.20</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>11.20-12.50</td>
                <td>1. Grup Toplantısı</td>
            </tr>
            <tr>
                <td>12.50-14.00</td>
                <td>Öğlen Arası</td>
            </tr>
            <tr>
                <td>14.00-15.30</td>
                <td>2. Grup Toplantısı</td>
            </tr>
            <tr>
                <td>15.30-16.00</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>16.00-17.30</td>
                <td>3. Grup Toplantısı</td>
            </tr>
            <tr>
                <td>17.30-18.00</td>
                <td>İlk Gün Kapanışı</td>
            </tr>
            <tr>
                <th style="font-size: 20px;">Gün 2 (5 Mart)</th>
                <th style="font-size: 20px;">Yeditepe</th>
            </tr>
            <tr>
                <td>10.00-10.30</td>
                <td>Kahvaltı</td>
            </tr>
            <tr>
                <td>10.30-12.00</td>
                <td>1. Komite Oturumu</td>
            </tr>
            <tr>
                <td>12.00-13.00</td>
                <td>Öğle Arası</td>
            </tr>
            <tr>
                <td>13.00-14.30</td>
                <td>2. Komite Oturumu</td>
            </tr>
            <tr>
                <td>14.30-14.50</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>14.50-16.00</td>
                <td>3. Komite Oturumu</td>
            </tr>
            <tr>
                <td>16.00-16.20</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>16.20-17.50</td>
                <td>Liderler Oturumu</td>
            </tr>
            <tr>
                <td>17.50-18.00</td>
                <td>İkinci Gün Kapanışı</td>
            </tr>
            <tr>
                <th style="font-size: 20px;">Gün 3 (6 Mart)</th>
                <th style="font-size: 20px;">Kültür Merkezi</th>
            </tr>
            <tr>
                <td>09.00-09.30</td>
                <td>Kahvaltı</td>
            </tr>
            <tr>
                <td>09.30-10.45</td>
                <td>Liderler Oturumu</td>
            </tr>
            <tr>
                <td>10.45-11.00</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>11.00-13.00</td>
                <td>Genel Kurul</td>
            </tr>
            <tr>
                <td>13.00-14.00</td>
                <td>Öğle Arası</td>
            </tr>
            <tr>
                <td>14.00-16.00</td>
                <td>Genel Kurul</td>
            </tr>
            <tr>
                <td>16.00-16.15</td>
                <td>Ara</td>
            </tr>
            <tr>
                <td>16.15-18.30</td>
                <td>Son Genel Kurul ve Dağılış</td>
            </tr>
        </table>
    </div>
</template>

<script>
import SectionLabel from './SectionLabel.vue'

export default {
    name: 'Day1Table',
    components: {
        SectionLabel
    }
}
</script>

<style scoped>
div {
    padding: 2vh 12vw;
}

table {
    border-collapse: collapse;
    width: 100%;
    padding-left: 10vh;
    padding-right: 10vh;
    padding-top: 10vh;
    padding-bottom: 10vh;
}

th,

td {
    text-align: left;
    padding: 8px;
}

tr:nth-child(even) {
    background-color: #f2f2f2;
}
</style>