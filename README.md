/*
-------------------- SCRIPT AUTO GENERATE URL RANDOM POST SAFELINK ------------------------------
Creator Coding : Usman Gamer
Web             : Cheegamer.Gq
Pesan           : Script ini dikhususkan untuk safelink buatan saya, kunjungi Cheegamer.gq untuk melihat project safelink lainnya. 
                  6 baris kode di bawah ini adalah kode untuk mengaktifkan fungsi script.
                  Tambahkan tag script dengan src=https://cdn.statically.io/gh/abdiusu/project-safelink-viomagz/f0c2c1ea/cryptojs-murni.js

script_auto_random_post = 'on';
direct_to_link = 'bunggsafelink.blogspot.com';
type_direct = 'all'; //all or only
no_direct_domain ='facebook.com,https://wa.me/923177184753,twitter.com,pinterest.com';
only_direct_domain = 'drive.google.com,domainlain.com';
type_target_click = '_blank'
path = '#?go=';
*/

if (script_auto_random_post == 'on') {
    var hasilgetlinkarp = false;
    $.ajax({
        url: '//' + direct_to_link + "/feeds/posts/summary/?alt=json-in-script&orderby=updated&max-results=9999",
        type: 'get',
        dataType: 'jsonp',
        success: function aku(younglex) {
            var cewek_cantik = younglex.feed;
            var ambillinku = cewek_cantik.openSearch$totalResults.$t;
            if (ambillinku > 150) {
                var totallinkarp = 150;
            };
            if (ambillinku <= 150) {
                var totallinkarp = ambillinku;
            };
            var listlinkku = new Array();

            for (var i = 0; i < totallinkarp; i++) {
                if (cewek_cantik.entry[i].link[14] === undefined) {
                    var akuula = cewek_cantik.entry[i].link[12].href;
                    if (akuula.indexOf(direct_to_link) >= 0) {
                        listlinkku[i] = cewek_cantik.entry[i].link[12].href;
                    }
                } else {
                    listlinkku[i] = cewek_cantik.entry[i].link[14].href;
                }

            }
            hasilgetlinkarp = listlinkku;
            nextgetarp();
        },
        async: false
    });

    function nextgetarp() {
        var long_bungabdi_tampan = document.getElementsByTagName('a').length;
        var bungabdi_tampan = new Array();
        var bungabdi_tampan2 = new Array();
        var kasian_si_jomblo = new Array();
        var kasian_si_jomblo2 = new Array();
        var filter_bungabdi_tampan = -1;
        var filter_bungabdi_tampan2 = -1;
        var filter_bungabdi_tampan3 = -1;
        if (type_direct == 'all') {
            fix_nodirect_domain = (no_direct_domain + ',' + window.location.hostname + ',blogger.com,javascript:void(0);').split(',');
            i_love_you1();

            function i_love_you1() {
                filter_bungabdi_tampan += 1;
                if (filter_bungabdi_tampan < long_bungabdi_tampan) {
                    var bertobatla = document.getElementsByTagName('a')[filter_bungabdi_tampan].href;
                    bertobatla = bertobatla.replace('http://', '');
                    bertobatla = bertobatla.replace('https://', '');
                    bertobatla = bertobatla.replace('www.', '');
                    bertobatla = bertobatla.replace('#', '');
                    bertobatla = bertobatla.replace('?', '');
                    bungabdi_tampan[filter_bungabdi_tampan] = bertobatla.split('/')[0];
                    kasian_si_jomblo[filter_bungabdi_tampan] = filter_bungabdi_tampan;
                    i_love_you1();
                } else {
                    i_love_you2();
                }
            }

            function i_love_you2() {
                filter_bungabdi_tampan2 += 1;
                if (filter_bungabdi_tampan2 < fix_nodirect_domain.length) {
                    i_love_you3(filter_bungabdi_tampan2);
                    i_love_you2();
                } else {
                    i_love_you4();
                }
            }
}
        //only_direct_domain
        if (type_direct == 'only') {
            for (var ji = 0; ji < only_direct_domain.split(',').length; ji++) {
                for (var i = 0; i < long_bungabdi_tampan; i++) {
                    var bungabdi_tampan2 = document.getElementsByTagName('a');
                    bungabdi_tampan[i] = bungabdi_tampan2[i].href.replace('http://', '').replace('https://', '').split('/')[0];
                    if (bungabdi_tampan[i].indexOf(only_direct_domain.split(',')[ji]) >= 0) {
                        var rajin_sholat_ya = document.getElementsByTagName('a')[i].href;
                        var ibuku_baik = aesCrypto.encrypt(convertstr(rajin_sholat_ya), convertstr('root'));
                        var mengantuk = hasilgetlinkarp[parseInt(Math.random() * hasilgetlinkarp.length)] + path + ibuku_baik;
                        document.getElementsByTagName('a')[i].setAttribute('href', mengantuk);
                        document.getElementsByTagName('a')[i].setAttribute('target', type_target_click);
                        console.log(only_direct_domain.split(',')[ji] + ' ada di posisi ' + i)
                    }
                }
            }
        }
    }

}
