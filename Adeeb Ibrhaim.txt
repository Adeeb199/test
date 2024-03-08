function checkData(input) {

  var checklines = input.split('\n');

  var numbers = parseInt(checklines[0], 10);

  var newData = [];

  for (let i = 1; i <= numbers; i++) {
      let [Number, String] = checklines[i].split(' ');

      newData.push({ num: parseInt(Number, 10), str: i > numbers / 2 ? String : '-' });
  }
 
  newData.sort((a, b) => a.num - b.num);

  var Twistresult = newData.map(data => data.str).join(' ');
  console.log(Twistresult);
}

const input = `20
0 ab
6 cd
0 ef
6 gh
4 ij
0 ab
6 cd
0 ef
6 gh
0 ij
4 that
3 be
0 to
1 be
5 question.
1 or
2 not
4 is
2 to
4 the`;

checkData(input);