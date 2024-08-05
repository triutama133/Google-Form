

#This code is used for create automatically dropdown update on Google-Form by user update


var ssID = "1P0lCkSWgpEPnRk-wvlVfSX2k3GbbI42EMbZgZ-_3QHM";
var formID = "1S0Vi56Wz69uBc5PjhXhwqqtXPhno66HMjQbDBLy2gbk";


var wsdata = SpreadsheetApp.openByUrl('https://docs.google.com/spreadsheets/d/1P0lCkSWgpEPnRk-wvlVfSX2k3GbbI42EMbZgZ-_3QHM/edit#gid=0');
  var ss= SpreadsheetApp.openByUrl('https://docs.google.com/spreadsheets/d/1P0lCkSWgpEPnRk-wvlVfSX2k3GbbI42EMbZgZ-_3QHM/edit#gid=0');
  var dataSheet = ss.getSheetByName("data");
var form = FormApp.openById(formID);



function myFunction() {
  
  var item = form.getItemById(943558618);
  Logger.log(item.getTitle());
  //var item = form.getItems();
  //Logger.log(item[1].getId().toString());
}

#next step

function myFunction() {
  
  var item = form.getItemById(1113489098);
  var values = ["Ujang","Udin"];
  item.asListItem().setChoiceValues(values);
  //var item = form.getItems();
  //Logger.log(item[12].getId().toString());
}

#nextstep
unction updateDropdownUsingTitle(title,values) {
  var title = "Nama Penggerak Lokal (Kab. Bandung)";
  var values = ["t","u","v"];
  var items = form.getItems();
  var titles = items.map(function(item){
    return item.getTitle();
  });

  var pos = titles.indexOf(title);
  var item = items[pos];
  var itemID = item.getId();

  
  updateDropdown(itemID,values)
}


function updateDropdown(id,values) {
  
  var item = form.getItemById(id);
  item.asListItem().setChoiceValues(values);
}
