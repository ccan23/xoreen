# xoreen
###### Read before using the program.

- ###### Xoreen's purpose and what it does
- ###### How it works
- ###### Xor Gate
- ###### Base64 Algorithm and Compatible Documents
- ###### Warnings
- ###### Installation
- ###### Contact Information, Version and License
- ###### Detailed Information About the Xor Gate

## Xoreen's Purpose and What it Does
The purpose of this program is to protect the desired documents in an unbreakable way.
## How it Works
The desired document is taken to a Xor Gate with a user determined key.The Xor Gate encrypts this document in a **recoverable** way. To recover it, the document must be taken to the Xor Gate with the **same** key that was used to encrypt the document. No other key can **_recover_** the original document.

## Xor Gate
Xoreen can interact with any document that the operating system can read or write.

##### *Xor Gate Confusion Matrix* : (a and !b) or (!a and b)
| A | B | A XOR B |
|---|---|:-------:|
| 0 | 0 |    0    |
| 0 | 1 |    1    |
| 1 | 0 |    1    |
| 1 | 1 |    0    |

The document's codepoints and the key's codepoints are passed through the Xor Gate.

##### *Simplified Graphical Representation:*
##### *Defined Keys*

| Character |  Binary   |
|:---------:|:---------:|
| c         | 01100011  |
| e         | 01100101  |
| n         | 01101110  |
| o         | 01101111  |
| r         | 01110010  |
| s         | 01110011  |
| t         | 01110100  |
| x         | 01111000  |

##### *Xor Encrpytion with a selected document and a key*

| String Status | String Name |                     String Binary                     |
|:-------------:|:-----------:|:-----------------------------------------------------:|
| Original      |  xoreen     | 01111000 01101111 01110010 01100101 01100101 01101110 |
| Key           |  secret     | 01110011 01100101 01100011 01110010 01100101 01110100 |
| Encrypted     |  undefined  | 00001011 00001010 00010001 00010111 00000000 00011010 |

##### *Decrypting the selected document with the correct key*

| String Status  | String Name |                     String Binary                     |
|:--------------:|:-----------:|:-----------------------------------------------------:|
| Encrypted      | undefined   | 00001011 00001010 00010001 00010111 00000000 00011010 |
| Key            | secret      | 01110011 01100101 01100011 01110010 01100101 01110100 |
| Original       | xoreen      | 01111000 01101111 01110010 01100101 01100101 01101110 |

## Base64 Algorithm and Compatible Documents

Base64 can encrypt binary data but UTF8 and UTF16 can only encrypt Unicode texts,
for this reason, in some cases Base64 algorithm can be used.

Since Base64 algorithm can transform almost any file format to UTF-8 characters, the transformed characters can pass through the Xor Gate .

**Any file format that can be processed with the Base64 algorithm can pass through the Xor Gate.**
>_.pdf, .mp3, .doc, .jpg, .png, vb..._

**Any compressed file can pass through the Xor Gate.**
> _.zip .rar, .tar.xz vb..._

#### Processing Base64 with the Xor Gate at the same time:

**Encoding Process(Encryption)**

`document --> base64 encode --> xor gate`

**Decoding Process(Decryption)**

`document--> xor gate --> base64 decode`

## Warnings

- Dont interrupt the program. A file that was broken during the encryption process  **_may not be recovered_**.
- Do not **_lose_** or **_forget_** the key. An encrpyted file **__cannot be recovered__** without a key.
- The Xor Gate is safest when the file's byte size is the same length as the key.
- To keep your key safe a random key can be generated.
.`--keygen`
- If a random key is not generated, it is suggested that log files be deleted from the terminal.`history -c` `history -w`
- Based on the processing speed, the process can be either quick or slow.

## Installation
- The following steps are valid for the Linux Distributations.
- Xoreen only requires a ruby compiler. If ruby is not installed:
>`sudo apt install ruby`
- If it is installed,give any permission you like to Xoreen.
> `sudo chmod 777 /root/xoreen/xoreen`
- put xoreen in the /usr/bin/ folder.
> `sudo cp /xoreen/xoreen /usr/bin/xoreen`

- xoreen does not use ruby gem but requires **getoptlong.rb** and **base64.rb** documents.
 - If ruby is up-to-date, then the files must be present. If it is not up-to-date or if the files are deleted, they can be found in the /xoreen/require/ folder.

 - If encountered with the Load Error:

  1. getoptlong.rb may be deleted.
  >`sudo cp /xoreen/require/getoptlong.rb /usr/lib/ruby/(user version)/getoptlong.rb`
  2. base64.rb may be deleted.
  >`sudo cp /xoreen/require/base64.rb /usr/lib/ruby/(user version)/base64.rb`

## Contact Information, Version ve License

- author : noycorp
- e-mail : noycorp@protonmail.com
- License: GPL v3 License
- Version: xoreen 1.0.0

**NOT:** If you've found any exploits or errors or if you have any suggestions, pleace contact me.


### Detailed Information about the Xor Gate

- [Xor Gate Image](https://www.khanacademy.org/computing/computer-science/cryptography/ciphers/a/xor-and-the-one-time-pad)
- [CodePoints](https://en.wikipedia.org/wiki/Code_point)
- [XorGate](https://en.wikipedia.org/wiki/XOR_gate)
- [XorCipher](https://en.wikipedia.org/wiki/XOR_cipher)
