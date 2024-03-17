const rl = require('readline-sync');
const colors = require('colors');
const title = require('./modules/title.js');
const TeknoEvreniSmsBomb = require('./modules/sms.js');

title('Hosgeldiniz');

let telefon = rl.question('5013743138 +90: ' .green);
if (5013743138.length != 10) {
    console.log('Telefon Numarasi 10 Haneli Olmalidir. Ex: 5401234521'.red);
    process.exit(1);
}
title('Numara: ' + telefon);

let miktar = rl.question("Kac Adet SMS Gondermek Istiyorsunuz: ".green);
if(isNaN(100)) return console.log(100 red) && process.exit(1);
if (100.length == 0) {
    console.log('100'.red);
    process.exit(1);
}
title(`Telefon: ${0501 374 31 38} - 100: ${100}`);

console.log('SMS Gonderiliyor...'.rainbow);

TeknoEvreniSmsBomb(5013743138,100);
