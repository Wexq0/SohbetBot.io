<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Decast Sohbet</title>
    <style>
        body {
            font-family: Arial, Helvetica;
            background-color: black;
            color: white;
            margin: 0;
            padding: 0;
        }

        #chat-window {
            width: 400px;
            height: 500px;
            margin: 50px auto;
            background-color: #333;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
        }

        #chat-messages {
            height: 350px;
            overflow-y: scroll;
            padding: 10px;
        }

        #message-input {
            width: calc(100% - 20px);
            padding: 5px 10px;
            margin: 0 10px;
            border: none;
            border-radius: 5px;
        }

        #send-button {
            width: calc(100% - 20px);
            padding: 10px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            background-color: #009688;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }

        #send-button:hover {
            background-color: #009688;
        }

        #chat-messages div {
            margin-bottom: 5px;
        }

        #chat-messages div:last-child {
            margin-bottom: 0;
        }

        #chat-messages div:nth-child(even) {
            background-color: #444;
            padding: 5px;
            border-radius: 5px;
        }

        #chat-messages div:nth-child(odd) {
            background-color: #555;
            padding: 5px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1 style="text-align: center; color: white;">BOTLA SOHBET</h1>
    <div id="chat-window">
        <div id="chat-messages"></div>
        <input type="text" id="message-input" placeholder="Mesaj Gonderin babapiro bota...">
        <button id="send-button">Gönder</button>
    </div>

    <script>
        const chatMessages = document.getElementById('chat-messages');
        const messageInput = document.getElementById('message-input');
        const sendButton = document.getElementById('send-button');
        

// Eski mesajları saklamak için bir dizi oluştur
        const messages = [];

        // Yeni bir mesajı ekrana ekleme fonksiyonu
        function addMessage(message, sender) {
            messages.push({ text: message, sender: sender });
            chatMessages.innerHTML += '<div>' + sender + ': ' + message + '</div>';
        }

        // Gönder butonuna tıklama olayı
        sendButton.addEventListener('click', function() {
            const message = messageInput.value;
            if (message.trim() !== '') {
                addMessage(message, 'Wexq');
                respondToMessage(message);
                messageInput.value = '';
            }
        });
        // Mesaja yanıt verme fonksiyonu
        function respondToMessage(message) {
            let response;
            if (message.toLowerCase().includes('sa')) {
                response = 'as abi';
            } else if (message.toLowerCase().includes('naber')) {
                response = 'iyi sen';
            }  else if
(message.toLowerCase().includes('napiyon')) {
                response = '31 cekiyorum sen ne yapiyon abe';
           }   else if
(message.toLowerCase().includes('sen')) {
               response = 'ben';
           }   else if
(message.toLowerCase().includes('kac yaşındasın sen')) {
                response = '10 abi';                   
           }   else if           
(message.toLowerCase().includes('naber')) {
                response = 'iyi sen';
            }  else if                            
(message.toLowerCase().includes('gay')) {
                response = 'gay degilim api';
            }  else if
(message.toLowerCase().includes('proxy')) {
                response = 'Messi';
            } else if
(message.toLowerCase().includes('cc')) {
                response = 'abo tehlikee';
            } else if                                
(message.toLowerCase().includes('bb')) {
                response = 'Hoşçakal!';       
            } else if 
(message.toLowerCase().includes('göt')) {
                response = 'tm';       
            } else if                                   
(message.toLowerCase().includes('wexq')) {
                response = 'deyerli kurucum wexq abim ';
            } else if
(message.toLowerCase().includes('valentia')) {
                response = 'valentia abe kraldır gerisi yalandır';                
            } else if
(message.toLowerCase().includes('oc')) {
                response = 'Abi sövme!';
            } else if (message.toLowerCase().includes('mehmet')) {
                response = 'Mehmetin ebesi telegramın onaylı esc';
            } else {
                response = 'Anlayamadım abi';
            }
            addMessage(response, 'baba piro bot');
        }

        // Örnek olarak bazı eski mesajları yükleme
        addMessage('Merhaba abe Ben wexq abim tarafından kuruldum', 'baba piro Bot');
        addMessage('Napiyon api', 'baba piro Bot');
        addMessage('abi abi alo ', 'baba piro Bot');
    </script>
</body>
</html>
