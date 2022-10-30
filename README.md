# Yara-Rules

rule APT_DoubleDragon_Installation {
{
   
   meta:
      Description = “APT DoubleDragon Installation”
      Author = “Lara Shakra”
      Reference = “https://attack.mitre.org/groups/G0096/,
      https://github.com/lshakra/Yara-Rules/new/main”
      Date = “10-30-2022”
      $hash1 = “04fb0ccf3ef309b1cd587f609ab0e81e”
      $hash2 = “fcfab508663d9ce519b51f767e902806”
      $hash3 = “0b2e07205245697a749e422238f9f785”
      $hash4 = “dd792f9185860e1464b4346254b2101b”
   
   strings:
      $d_1 = “ agegamepay.com”
      $d_2 = “ microsOff.com”
      $a_1 = “185.14.29.72”
      $a_2 = “23.67.95.153”
   
   condition:
      All of ($d*) OR
      All of ($a*) }
}
