# MVVM ViewModel

ViewModel is the heart of the pattern and was wittily titled [converter on steroids](https://joshsmithonwpf.wordpress.com/2008/12/01/the-philosophies-of-mvvm/).

ViewModel shall be fully unaware of presentation details - any UX declarations here (colors, sizes, layout, sounds/volume i.a.) are **definitely** wrong.\
It ought to be *info*, *alarm*, *warning*, *timeout*, *off-line*, *trusted*. And the View shall care about turning them into proper UX elements.

As well ViewModel shall not outline ways of UI arrangement and interaction (windows, panes, overlays, prompts).<sup>:raising_hand:</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup><sub>&nbsp;Could be redundant to say but still a common mistake.</sub>


## Notification grouping (orchestration)

## ViewModel-Model cohesion

## Messaging within MVVM
### Commands
### Dialogs
