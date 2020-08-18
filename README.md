PictureBox
==========
An open-source audio sampler project based on RaspberryPi.

A work in progress fork of the amazing project by Jospeh Ernest
(samplerbox.org). Currently I am making some mods for personal use to the project
and I thought I'd share my work as I go.

This modification allow for multiple samples to be play at the same time via explicit midi channels.

[Install](#install)
----

PictureBox works with the RaspberryPi's built-in soundcard, but it is recommended to use a USB DAC (such as [this 6€ one](http://www.ebay.fr/itm/1Pc-PCM2704-5V-Mini-USB-Alimente-Sound-Carte-DAC-decodeur-Board-pr-ordinateur-PC-/231334667385?pt=LH_DefaultDomain_71&hash=item35dc9ee479)) for better sound quality.

1. Install the required dependencies (Python-related packages and audio libraries):

  ~~~
  sudo apt-get update ; sudo apt-get -y install git python-dev python-pip python-numpy cython python-smbus portaudio19-dev libportaudio2 libffi-dev
  sudo pip install rtmidi-python pyaudio cffi sounddevice
  ~~~

2. Download PictureBox and build it with: 

  ~~~
  git clone https://github.com/PictureOneMusic/PictureBox.git
  cd PictureBox ; sudo python setup.py build_ext --inplace
  ~~~

3. Run the soft with `python picturebox.py`.

4. Play some notes on the connected MIDI keyboard, you'll hear some sound!  

5. Send multiple channels of midi and hear different sounds!

*(Optional)*  Modify `picturebox.py`'s first lines if you want to change root directory for sample-sets, default soundcard, etc.


[About](#about)
----
Forked from:

Author : Joseph Ernest (twitter: [@JosephErnest](http:/twitter.com/JosephErnest), mail: [contact@samplerbox.org](mailto:contact@samplerbox.org))


[License](#license)
----

[Creative Commons BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
