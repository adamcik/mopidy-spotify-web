*********************
Mopidy-Spotify-Web
*********************


`Mopidy <http://www.mopidy.com/>`_ extension for providing the browse feature
of `Spotify <http://www.spotify.com/>`_. This lets you browse artists and albums
of your spotify user account library.

Uses the `Spotipy <https://github.com/plamere/spotipy/>`_ API, which is a python wrapper arround
the spoitify web api.


Dependencies
============

- A Spotify Premium subscription. Mopidy-Spotify will not work with
  Spotify Free, just Spotify Premium.

- A non-Facebook Spotify username and password.

- ``Mopidy`` >= 0.19.0. The music server that Mopidy-Spotify-Tunigo extends.

- ``Mopidy-Spotify`` >= 1.2.0. The Mopidy extension for playing music from
  Spotify.

- ``Spotipy``. A library for accessing the Spotify web-api.


Installation
============

install the package from PyPI::

    pip install Mopidy-Spotify-Web


Configuration
=============

To run this extension you need to authorize it against you Spotify account, to do this visit
https://www.mopidy.com/authenticate/#spotify and follow the instructions.

Example configuration::

    [spotify_web]
    client_id = ... client_id value you got from mopidy.com ...
    client_secret = ... client_secret value you got from mopidy.com ...

The following configuration values are available:

- ``spotify/enabled``: If the Spotify extension should be enabled or not.
  Defaults to ``true``.

- ``spotify_web/client_id``: Your Spotify application client id. You *must* provide this.

- ``spotify_web/client_secret``: Your Spotify application secret key. You *must* provide this.

- ``spotify_web/token_url``: url to the authorization endpoint
  of the Mopidy OAuth bridge for Spotify. Defaults to https://auth.mopidy.com/spotify/token.


Project resources
=================

- `Source code <https://github.com/lfcabend/mopidy-spotify-web>`_
- `Issue tracker <https://github.com/lfcabend/mopidy-spotify-web/issues>`_
- `Download development snapshot <https://github.com/lfcabend/mopidy-spotify-web/archive/master.tar.gz#egg=Mopidy-Spotify-Web-dev>`_


Changelog
=========

v0.2.0 (unreleased)
-------------------

- Use ``requests`` module for fetching tokens.
- Blocking initialization moved out of critical startup path.
- Various internal cleanups to make code more Pythonic.
- Switch to using Mopidy's token swap service for simpler authentication.

v0.1.0 (2015-05-03)
-------------------

- Initial release.
