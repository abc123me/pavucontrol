# Pavucontrol (fork)

My goal with this fork is to add audio priorities to pavucontrol, similar to the
audio priorities that used to be in teamspeak.

I barely understand GTK and I have no understanding of the internals of pulseaudio so there
is no way this will get done in a reasonable timespan.

What I have done so far:
 - Added the button for priorities to the UI
 - Added a callback for said button
 - Created a plan of action for doing this
   - Watch the peak volumes of all priority applications, whenever they are
     louder then a set threshold mute all other applications.

Compilation:
 - Run `autogen.sh`
 - Run `configure`
 - Run `make`, then `make install` as root
 - Make sure to have `intltool`
