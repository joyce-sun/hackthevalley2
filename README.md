class Network:
    def __init__(self):
	    “”” Initialize a new Network class.”””
	    self.barcode = None
        self.search = None

    def __str__(self):
	    “”” Return a str representation of self “””
	
    def __eq__(self):
	    “”” Determines whether self is equivalent to other “””
	    return type(self) == type(other) and self.barcode == other.barcode and self.search == other.search
    def search
    def barcode
    def scan_barcode

class SocialMedia(Network):
    def __init__(self):
	    “”” Initialize a SocialMedia class.”””
    def __str__(self):
    def __eq__(self):
    def email
    def phone_number
    def twitter
    def facebook
    def instagram
    def snapchat
    def linkedin

class CreateUser:
    def __init__(self, name, username, email, password):
	    “”” Initialize a CreateUser class.”””
	    self.name = CurrentState(input(“Input your full name.”))
	    self.username = CurrentState(input(“Input a unique username”))
        self.email = CurrentState(input(“Input your email address”))
        self.password = CurrentState(input(“Input your password”))
    def __str__(self):
    def __eq__(self):
    def check_user(self) -> bool:
	“”” Return True if the username inputted is unique to the software
	>>> a = CreateUser()
	>>> a.check_user(“jerry”)
	True
    ”””
	
def check_password(self, ) -> bool:
    “””Return True if password is Valid. A valid password must be at least 6 characters, one number and one capital 
    letter. A valid password must only contain numbers and letters.
    >>> check_password(“Rochelle3”)
    True
    >>> check_password(“cat-”)
    False
    >>> check_password(
    ”””

class CurrentState:
    def __init__(self, name: str, username: str, email: str, password: str):
        “””Initialize a new CurrentState class”””
        self.name = name
        self.username = username
        self.email = email
        self.password = password
    def change_password
    def change_username
    def change_name
    def change_email

class Display:
    def __init__(self):
    def __str__(self):
    def __eq__(self):
    def name
    def photo
    def barcode
    def username
    def social_media

