Strongbox.rb
============

Ruby script for decrypting and reading www.Strongbox.io files from the command line

Description
-----------

**Strongbox** (https://www.strongbox.io/) provides a simple way to effectively
organize, secure, and share sensitive textual data, the kind that has no other
home: passwords, credentials, credit card & account numbers, encryption keys,
certificates, etc. - essentially, anything we're not comfortable simply putting
into an unencrypted text document file or sharing via email, Skype, etc.

**This Ruby script** (`strongbox.rb`) enables decrypting and reading Strongbox
files from the command line. It depends on the gems
[strongboxio](https://github.com/abatko/strongboxio) (for decrypting and
reading Strongbox files) and `highline` (for command-line i/o).

Setup
-----

 * `gem install strongboxio`
 * `gem install highline openssl zlib base64 nokogiri` # the dependencies
 * download this Ruby script (`strongbox.rb`)
 * mv ~/Downloads/strongbox.rb ~/bin/ # place this script in a suitable directory
 * chmod u+x ~/bin/strongbox.rb # give yourself permission to execute this script

Examples
--------

These examples assume `strongbox.rb` is executable and in a directory in PATH.

    $ strongbox.rb 
    Usage /Users/abatko/bin/strongbox.rb input.sbox

    $ strongbox.rb the_case_of_everything.sbox
    Enter the password to unlock this box: ********
    2012-11-27T23:29:23.18873Z
    
    VanCity bank info
    credit card, debit card, online banking
    Credit, Debit, Card, Online, Banking
    credit card number: 
    1234 5678 9012 3456
    credit card expiration: 
    11/2012
    credit card verification value: 
    123
    debit card PIN: 
    1234
    online banking password: 
    qwerty
    
    fake Gmail account
    used for Stackoverflow
    Fake Gmail Stackoverflow
    username: 
    ima_fake@gmail.com
    password: 
    password1
    gender: 
    other
    backup: 
    bart_simpson@gmail.com

