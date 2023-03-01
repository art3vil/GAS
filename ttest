let token ="your token";

function getMe() {
  let response =  UrlFetchApp.fetch("https://api.telegram.org/bot" + token + "/getMe");
  console.log(response.getContentText());
}

function setWebHook() {
  let webAppUrl = "your url";
  let response =  UrlFetchApp.fetch("https://api.telegram.org/bot" + token + "/setWebHook?url="+ webAppUrl);
  console.log(response.getContentText());
}

function sendText(chat_id, text){
  let data = {
    method: "post",
    payload: {
      method: "sendMessage",
      chat_id: String(chat_id),
      text: text,
      parse_mode: "HTML"
    }
  };
  UrlFetchApp.fetch("https://api.telegram.org/bot" + token + "/", data);
}

function send() {
  let chat_id = your tg id;
  let text = "hello world"
  sendText(chat_id, text);
}


function doPost(e) {
  let contents = JSON.parse(e.postData.contents);
  let chat_id = contents.message.chat.id;
  let text =contents.message.text;
  sendText(chat_id, text);
  SpreadsheetApp.openById("your sheet id).getSheetByName("Messages").appendRow([chat_id, text]);
}
