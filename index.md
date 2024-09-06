
# Demonstrating RSA Encryption with GnuPG and Kleopatra

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Introduction

This first part of the paper is dedicated to explaining and analyzing the steps that were taken for this lab. The objective here is to introduce the basic methods used for encrypting messages and files. In this case, we will focus only on RSA encryption and how it is able to encrypt and decrypt simple text files. I will be using an open-source software known as Gpg4win and its certificate managing tool Kleopatra to carry out this process. I will begin by first explaining the installation and setup of Gpg4win and then go into detail about creating the OpenPGP key pair I will be using. From there, I will describe the processes of encryption and decryption and finally conclude with some final reflections.

## Installing Gpg4win and Preparing for Encryption

Before I can start any work with encryption, I must first set up my workspace. The only things I need are my email, a text editor (in this case, Notepad), and a software known as Gpg4win. To be specific, I will be using Gpg4win version 3.1.15. According to the “about” page on its website, Gpg4win is an open-source software that enables users to securely transport emails and files with the help of encryption and digital signatures (Gpg4win). As the name suggests, this software’s focus is to implement GNU Privacy Guard and its features into Windows. This will be the primary tool for the lab as it will be handling all of the encoding and decoding. Although Gpg4win is referred to as a singular unit, it is actually made up of several smaller components: GnuPG the encryption tool, Kleopatra the certificate manager, GpgOL and GpgEX for additional email and file encryption, and GPA, another certificate manager. For this lab, I will only be using Kleopatra and GnuPG for key creation, certification management, and message encryption (and for the sake of precision, I will be referring to these programs separately).

 Once the software has been installed, I am now ready to begin the first steps of encryption. The directions for this lab specify that I will be working with RSA encryption. To provide a brief overview, RSA encryption is a type of asymmetric encryption in which a message is encrypted with a public key anyone can use and decrypted with a private key that the intended recipient possesses (Lake). The process of RSA is as follows: First, a public and private key pair is generated. The most common method of generating this key pair is through equations that deal with extremely large prime numbers. The idea here is that the end result is easy to see but to figure out the individual parts would be nearly impossible. After the keys have been created, the next step is to use the public key to encrypt the message. Once the message has been encrypted, it is now scrambled based on the key’s algorithms and is indecipherable. From there, the message can now travel through the network to its intended recipient who then decrypts it with his or her own private key. The process concludes with the message being restored to its original form. The perk of RSA encryption is that the message’s contents are totally hidden when it is encrypted. Even if an intruder were to intercept it, the message would be unusable to him or her without the proper private key. This lab will demonstrate this process thusly except that it will be in a more simplified form.

## Creating the Public and Private Key Pair and Exchanging Public Keys

Upon running the Gpg4win executable file, the GUI for Kleopatra is opened. As mentioned, this is the certificate manager, and I will be using it for creating and importing key pairs for encryption and decryption. The first step, however, is to create the keys. Rather than having to deal with complex algorithms, Kleopatra has a more simplified process in that it uses a Creation Wizard to automatically generate a key pair given only a few key pieces of information. The user needs only to provide his or her name, an email address, and, if they wish, specifications on the form of encryption and for what purpose(s) it will be used. The figure below shows the creation process for my own key pair:

- <dt>Figure 1</dt>: Here we see the GUI for Kleopatra along with the basic and advanced dialogue windows for creating a new key pair. My name and email are filled out in the first window and the advanced window is filled out according to the lab instructions. This key pair will only be used for encryption (it will not sign or authenticate) and is valid until June 6, 2021.
### Java Shit
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
