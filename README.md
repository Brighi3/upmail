

# Login a 2 fattori di autenticazione
Il programma è un'applicazione web basata su Flask che implementa un sistema di autenticazione utilizzando username, password e una One-Time Password (OTP). 
L'obiettivo è verificare l'identità dell'utente richiedendo username e password, inviare un codice OTP all'indirizzo email specificato e successivamente verificare anche il codice OTP inserito dall'utente per 
concedere l'accesso.



## Funzionalità

L'utente accede alla pagina principale dell'applicazione. Qui viene presentato un modulo di accesso che richiede l'username e la password.

L'utente inserisce l'username e la password e invia il modulo. Il server Flask verifica se l'username e la password corrispondono alle credenziali memorizzate (nel caso di esempio, l'username è "[nostronome@gmail.com]" 
e la password è "1234"). Se le credenziali sono corrette, viene generato un codice OTP casuale.

Il server Flask invia il codice OTP all'indirizzo email specificato. 
Questo viene fatto utilizzando la funzione send_otp_email() che utilizza la libreria smtplib per inviare l'email tramite un server SMTP configurato.

L'utente viene reindirizzato alla pagina di verifica dell'OTP. Qui viene richiesto di inserire l'OTP ricevuto via email insieme al proprio username.

L'utente inserisce l'OTP e l'username e invia il modulo. Il server Flask recupera l'OTP memorizzato per l'utente specificato utilizzando la funzione get_stored_otp().

Il server Flask verifica se l'OTP inserito dall'utente corrisponde all'OTP memorizzato. Se corrispondono, viene visualizzata una pagina di conferma con il messaggio "Accesso effettuato correttamente". 
In caso contrario, viene visualizzato un messaggio di errore.

## Installazione
