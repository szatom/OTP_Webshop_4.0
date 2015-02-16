# OTP_Webshop_4.0
Patch for deprecated static call for not static function

1) The Webshop files have Dos/Windows base CR-LF end of file. You have to convert to CL. On MAC OS:
find ./ -type f -name '*.php' -print0 | xargs -0 -I {} perl -pi -e 's/\r\n/\n/g' {}
2) Apply patch:
patch -p1 < non-static-method-fix.patch
