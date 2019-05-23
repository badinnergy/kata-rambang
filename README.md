# kata-rambang

`kata-rambang` ialah sebuah JS program yang secara rambang, menjana perkataan Bahasa Melayu (perkataan biasa & tidak biasa).

`kata-rambang` ialah JS program yang sama dengan [`random-words`] (https://www.npmjs.com/package/random-words)

Bezanya ialah `kata-rambang` jana perkataan Bahasa Melayu bukannya perkataan Inggeris.

`kata-rambang` is a JS program that generates common & uncommon Malay words, randomly.

`kata-rambang` is the same JS program as [`random-words`] (https://www.npmjs.com/package/random-words)

The only difference is `kata-rambang` generates Malay words instead of English words.

## Generate Malay words


Installation:

    npm install kata-rambang

Examples:

    var rambang = require('kata-rambang');

    console.log(rambang());
    arang

    console.log(rambang(5));
    ['maki', 'pukul', 'mencaplok', 'dialek', 'menyikat']

    console.log(rambang({ min: 3, max: 10 }));
    ['awam', 'limbat', 'autopsi', 'empat']

    console.log(rambang({ exactly: 2 }));
    ['jumpa', 'cepat']

    console.log(rambang({ exactly: 5, join: ' ' }))
    'buntu tok sandiwara kemiliteran besar'
    
    console.log(rambang({ exactly: 5, join: '' }))
        'rentaksahsengmurahterkenal'

    console.log(rambang({exactly: 5, maxLength: 4}))
    ['war','pel','toh','wan','sana']

    console.log(rambang({exactly:5, wordsPerString:2}))
    [ 'po khasiat', 'konvensyen perincian', 'menari bekalan', 'mengharumkan revolusioner', 'penyelarasan gelap' ]

    console.log(rambang({exactly:5, wordsPerString:2, separator:'-'}))
    [ 'ditentukan-serigala', 'sepanyol-asasi', 'algebra-nakhoda', 'kakanda-landa', 'tahunan-membunuh' ]

    console.log(rambang({exactly:5, wordsPerString:2, formatter: (word)=> word.toUpperCase()}))
    [ 'BOT KEKAR', 'JERMAN BERPILIH', 'KALKULASI ADUHAI', 'RESTORASI PAUTAN', 'TUALA TAYAR' ]

    console.log(rambang({exactly:5, wordsPerString:2, formatter: (word, index)=> {
        return index === 0 ? word.slice(0,1).toUpperCase().concat(word.slice(1)) : word;
    }}))
    [ 'Emigrasi rebana', 'Tangis sebaliknya', 'Pulangan perihal', 'Alergi mengancam', 'Menembak median' ]
