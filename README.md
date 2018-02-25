from typing import Any
import pyqrcode
import qrtools
from PIL import Image
import zbarlight

class Network:
   """Network Class"""
   def __init__(self) -> None:
        """
        Initialize a new Network class
        """
        self.barcode = None
        self.search = None

   def __eq__(self):
        """
        Determines whether self is equivalent to other
        """
        return type(self) == type(other) and \
               self.barcode == other.barcode and \
               self.search == other.search

   def qr_generator(self):
        """
        Create a unique QR code for a user
        """
        q = pyqrcode.create(str(username))
        q.png('myQR.png', scale=6)

   def qr_reader(self):
        """
        Scan QR code
        """
        file_path = './tests/fixtures/two_qr_codes.png'
        with open(file_path, 'rb') as image_file:
            image = Image.open(image_file)
            image.load()

        codes = zbarlight.scan_codes('qrcode', image)
        print('QR codes: %s' % codes)

class SocialMedia:
   """Social Media Class"""
   list_display = ('twitter', 'facebook', 'linkedin')

   def __init__(self):
        """Initialize a SocialMedia class."""

   def __str__(self, other: Any) -> bool:
       """Return True if self is equivalent to other"""
       return type(self) == type(other)

   def twitter(self, obj):
        """Create Twitter button/link"""
        return '''<a href="https://twitter.com/share" class="twitter-share-button" data-url="{}" data-text="{}"
                data-hashtags="{}" data-via="bedjango">Tweet</a>
                <script>
                    !function (d, s, id) {{
                        var js, fjs = d.getElementsByTagName(s)[0], p = /^http:/.test(d.location) ? "http" : "https";
                        if (!d.getElementById(id)) {{
                            js = d.createElement(s);
                            js.id = id;
                            js.src = p + "://platform.twitter.com/widgets.js";
                            fjs.parentNode.insertBefore(js, fjs);
                        }}
                    }}(document, "script", "twitter-wjs");
                </script>'''.format(obj.short_url, obj.title, obj.tags)

   def facebook(self, obj):
        """Create Facebook button/link"""
        return '''<div class="fb-share-button" data-href="{}" data-layout="button" data-size="small" 
	data-mobile-iframe="true">
               <a class="fb-xfbml-parse-ignore" target="_blank"
               href="https://www.facebook.com/sharer/sharer.php?/
	       u=http%3A%2F%2Fwww.emergya.com%2F&amp;src=sdkpreparse">Share</a>
               </div>
               <script>
                   (function(d, s, id) {{
                   var js, fjs = d.getElementsByTagName(s)[0];
                   if (d.getElementById(id)) return;
                   js = d.createElement(s); js.id = id;
                   js.src = "//connect.facebook.net/es_ES/sdk.js#xfbml=1&version=v2.7";
                   fjs.parentNode.insertBefore(js, fjs);
                   }}(document, "script", "facebook-jssdk"));
               </script>'''.format(obj.short_url)
	       
   def linkedin(self, obj):
        """Create Linkedin button/link"""
        return '''<div style="display:inline;">
               <script src="//platform.linkedin.com/in.js" type="text/javascript"> lang: en_US</script>
               <script type="IN/Share" data-url="{}"></script>
               </div>'''.format(obj.short_url)

   twitter.allow_tags = True
   twitter.short_description = 'Twitter'
   facebook.allow_tags = True
   facebook.short_description = 'Facebook'
   linkedin.allow_tags = True
   linkedin.short_description = 'Linkedin'

class CreateUser:
   """ A CreateUser Class."""

   def __init__(self) -> None:
        """
        Initialize a CreateUser class.
        """
        self.name = input("Input your full name.")
        self.email = input("Input your email address")
        self.password = input("Input your password")

   def __str__(self):
        """Returns a str representation of self"""
        return ""

   def __eq__(self, other: Any):
        """ Checks whether self is equivalent to other
        """
        return type(self) == type(other)

   def check_password(self) -> bool:
        """Return True if password is Valid. A valid password must be at least 6 characters, one
        number and one capital letter. A valid password must only contain numbers and letters.
        """
        upper = False
        num = False
        for ch in self.password:
            if ch.isupper():
                upper = True
            if ch.isalnum():
                num = True
        return (len(self.password) >= 6) and upper and num


class CurrentState:
   """CurrentState Class"""
   def __init__(self, name: str, email: str, password: str) -> None:
        """Initialize a new CurrentState class"""
        self.name = name
        self.email = email
        self.password = password

   def change_password(self, password: str) -> None:
        """Change password and ensure it is a valid password before and after"""
        if check_password(password):
            self.password = password

   def change_name(self, new_name: str) -> None:
        """Change the members name to a new name"""
        self.name = new_name

   def change_email(self, new_email: str) -> None:
        """Change the members email to a new email."""
        self.email = new_email

