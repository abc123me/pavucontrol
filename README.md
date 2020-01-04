# Pavucontrol (fork)

My goal with this fork is to add audio priorities to pavucontrol, similar to the
group leader priorities that used to be in teamspeak (when VoIP software actually was good).

Essentially the modification would lower the volume for applications that aren't priority, but
only when a prioritized application is making sound.

What I have done so far:
 - Added the button for priorities to the UI
 - Added a callback for said button
 - Created a plan of action for doing this
   - Watch the peak volumes of all priority applications, whenever they are
     louder then a set threshold mute/slowly lower all other applications.

Compilation:
 - Run `autogen.sh`
 - Run `configure`
 - Run `make`, then `make install` as root
 - Make sure to have `intltool`

Use cases:
 - Gaming (listening to music while playing CS, you *should* want to hear your team as clearly as possible)
 - Voice chats (you can prioritize the voice chat over any background applications)

I barely understand GTK and I have no understanding of the internals of pulseaudio so there
is no way this will get done in a reasonable timespan.
