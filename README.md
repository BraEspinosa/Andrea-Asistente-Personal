# ANDREA ASISTENTE PERSONAL

Andrea is a personal assistant, programmed in python and able to work in every linux device 

This repository contents:

  - Source codes
  - dev scripts(Python)
  - Andrea´s voice packs

# Hardware elements

  - Device with linux
  - Microphone

# Sofware Requirements

  - Python 3.2

# Install PyAudio

Installing the dependencies in python3, executed in terminal:

```sh
$ sudo apt-get install python-pyaudio python3-pyaudio
```

It is necessary install lastest PyAudio version, hence download PyAudio-0.2.11.tar.gz from the link https://pypi.python.org/pypi/PyAudio#downloads and execute in file direction:

```sh
$ sudo python setup.py install
```

# Install SpeechRecongnition

First, make sure you have Python3, then execute the command:

```sh
$ pip install SpeechRecognition
```

# Repository Folders

    /your_root        - path
    |--data           / Data base
    |--PyAudio        / Install PyAudio last version
    Andrea.py         / Main script
    
# Use Folders

In folder where was download the file, execute Andrea.py in terminal.

# How To Config

To send messages from your own e-mail, write your e-mail address and password:

```sh
def correo():
    print('A quien lo envias?')
    playsound('ElegirContacto.wav')
    enviado=0
    quien=microfono()
    contacto=lista()
    for i in range(len(contacto)):
        number=str(contacto[i,1])
        if str(quien)==str(contacto[i,0]):
            To = str(number+"@**********.com")
            print('Agregue Asunto')
            playsound('Asunto.wav')
            text=microfono()
            Asunto = str(text)
            print('Mensaje a enviar')
            playsound('Mensaje.wav')
            text=microfono()
            Mensaje = str(text)
            # create message object instance
            msg = MIMEMultipart()
            message = Mensaje
            # setup the parameters of the message
            password = "*******"
            msg['From'] = "*******@*******.com"
            msg['To'] = To
            msg['Subject'] = Asunto
            # add in the message body
            msg.attach(MIMEText(message, 'plain'))
            #create server
            server = smtplib.SMTP('smtp.gmail.com: 587')
            server.starttls()
            # Login Credentials for sending the mail
            server.login(msg['From'], password)
            # send the message via the server.
            server.sendmail(msg['From'], msg['To'], msg.as_string())
            server.quit()
            enviado=1
            print("successfully sent email to %s:" % (msg['To']))
            playsound('MensajeEnviado.wav')
```
# Autors

  - Harold F. Murcia - (www.haroldmurcia.com)
  - Brahian Steven Espisonsa Ruiz - (2420151009@estudiantesunibague.edu.co)
  - Andres Sebastian Salazar Alturo -(2420151021@estudiantesunibague.edu.co)




