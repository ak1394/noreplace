noreplace
=========

To get current replacements go to http://leprosorium.ru/fraud/textomate/usages/1 (and subsequent pages) and run following code in the Developer Tools/Javascript Console or Firebug:

var words = $(document.body).getElements('.fraud_one_word');
var r = {};
words.filter(function(w) { return !!w.getElements('td.fow_to_word')[0]; }).forEach(function(w) { 
  r[$(w).getElements('td.fow_to_word')[0].innerHTML] = $(w).getElements('td.fow_word')[0].innerHTML; 
});
console.log([r].toJSON());

