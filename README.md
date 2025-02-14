# Simple base45 encoder/decoder.

Qr and Aztec code have a specific, highly efficient, method for storing alphanumeric characters (MODE 2/0010). In particular compared to UTF-8 (where the first 32 characters are essentially unused; and successive non-latin characters loose an additional 128 values as the topbit needs to be set).

Details of this 11 bits per two characters can be found at

* https://www.thonky.com/qr-code-tutorial/alphanumeric-mode-encoding
* https://raw.githubusercontent.com/yansikeim/QR-Code/master/ISO%20IEC%2018004%202015%20Standard.pdf - section 7.44 on page 26

For this reason - the industry generally encodes these in base45. A document for this defacto standard is in flight:

    ```https://datatracker.ietf.org/doc/draft-faltstrom-base45/```
