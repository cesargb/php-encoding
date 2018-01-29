# PHP encode files
PHP class to encode filters

## Usage
construct($encoding_to = 'UTF-8', $encodings_detected = 'UTF-8,ISO-8859-1,WINDOWS-1252');
EncodeFile($fileR, $fileW, &$encoding_original, &$encoding_final);



This is an example:

'''php
include 'src/codification.php';

$codification = new Codification();

$fileR = "file.txt";
$fileW = 'fileEncoded.' . pathinfo($fileR, PATHINFO_EXTENSION);
$encoding_original = "";
$encoding_final = "";

$result = $codification->EncodeFile($fileR, $fileW, $encoding_original, $encoding_final);

if($result)
    echo "Conversión correcta." . '<br>';
else
    echo "Error en la conversión." . '<br>';

echo "Codificacion original: " . $encoding_original . '<br>';
echo "Codificación final: " . $encoding_final . '<br>';
'''

## Encoding values

### Allowed values
http://php.net/manual/es/mbstring.supported-encodings.php

### Default values
$encoding_to = 'UTF-8';
$encodings_detected = 'UTF-8,ISO-8859-1,WINDOWS-1252';
