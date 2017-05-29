
# Timers

This tutorial video covers how to create a small whack-a-mole game in WPF.

The way whack-a-mole works is that based on a timer, each button changes to a "hit me" colour. This tutorial focuses on setting up a `Timer` object where at a set interval, the object will fire an event (e.g. `Elapsed`). You respond to the `Elapsed` as a way of getting notified when the timer ticks out.

There are at least [five different timers in .NET](https://stackoverflow.com/questions/10317088/why-there-are-5-versions-of-timer-classes-in-net). Each has slightly different behaviour and semantics. The tuorial video shows the use of the `Sytsem.Timers.Timer`, which requires the use of an `Invoke` method to interact with the UI thread. An alternative is to use the `System.Windows.Threading.DispatchTimer`, which operates on the thread that it was called on. Using the `DispatchTimer` means you don't need to use the `Invoke` functionality.

[](https://youtu.be/O2o0CBx2hto)

([Tutorial 2 video](https://youtu.be/O2o0CBx2hto))
