# Google-Form

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
