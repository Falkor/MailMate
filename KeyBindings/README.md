-*- mode: markdown; mode: visual-line; fill-column: 80 -*-
`README.md`

Copyright (c) 2015 [Sebastien Varrette](mailto:<Sebastien.Varrette@uni.lu>)

      Time-stamp: <Wed 2015-11-11 15:35 svarrette>

------------------------------
# Falkor MailMate KeyBindings

* [Reference Documentation](http://manual.mailmate-app.com/custom_key_bindings)
* [List of Key Binding Selectors](http://manual.mailmate-app.com/key_binding_selectors)


Once of the killing feature of [MailMate](http://mailmate-app.com) is the complete freedom left to configure [custom key bindings](http://manual.mailmate-app.com/custom_key_bindings).
You can configure the `Falkor` key-bindings by placing the file [`Falkor.plist`](Falkor.plist) in:

```sh
~/Library/Application Support/MailMate/Resources/KeyBindings
```

Then relaunch [MailMate](http://mailmate-app.com) and set the shortcut in the preferences pane (`MailMate > Preferences... > General > Custom Key Bindings > Enable`). Enable the key bindings that you want by entering them in the box below, e.g. `Falkor`.

I have inspired from many resources online:

* [Keyboard shortcuts for Gmail](http://mail.google.com/support/bin/answer.py?answer=6594)
* [Jeremy Cowgar's MailMate keybindings](http://jeremy.cowgar.com/2014/09/22/my-mailmate-keybindings/)
* [Chauncey Garrett's MailMate Keybings](https://github.com/chauncey-garrett/mailmate/blob/master/README.md#key-bindings)

I shall also thank Mailmate's developper [Benny Kjær Nielsen](http://freron.com/about/index.html#about_me) for helping me on solving various issues when designing these key bindings.

## General Key Bindings Rules

| Shortcut | Code | Description |
| -------- | ---- | ----------- |
| a        | a    | -           |
| ⌃ a      | ^a   | Control-a   |
| ⌥ a      | ~a   | Option-a    |
| ⇧ a      | A    | Shift-a     |
| ⌘ a      | @a   | Command-a   |

From the [reference documentation](http://manual.mailmate-app.com/custom_key_bindings):

>In addition to the above, `$` can be used to bind to the shift key (`⇧`) for non-letter-keys and `#` can be used for the numeric key pad. Note that the order of multiple modifiers is important. It must be in this order: **`#^~$@`**

You will also find elements demonstrating the usage of the `ExpectReply` tag. Actually, I follow the workflow proposed in [this blog post](http://jeremy.cowgar.com/2014/09/18/mailmate-waiting-on-reply/) with the definition of '`Expect a Reply`' / '`Has Answer`' Smart mailboxes. 

## Sending Messages

| Shortcut | Action         | Description                                                      |
| :------: | -------------- | ---------------------------------------------------------------- |
| ⌘ ↩      | Send message   | After composing your message, use this combination to send it.   |
|          |                |                                                                  |

## Email Composition

| Shortcut | Action                | Description                                                                   |
| :------: | --------------        | ----------------------------------------------------------------              |
| c        | __C__ompose           | Allows you to compose a new message.                                          |
| r        | __R__eply             | Replies to the message sender, with a message starting by `Dear <firstname>,` |
| R (⇧ r)  | __R__eply to Sender   | Replies to the message sender (useful in a mail having multiple recipents)    |
| a        | Reply __a__ll         | Replies to all message recipients.                                            |
| f        | __F__orward           | Forwards a message.                                                           |
| F (⇧ f)  | __F__orward as Attachment | Forward selected message as an attachment (useful to respect the layout)      |
| ⌘ )      | Increase quote level  | Increase the quote level of the selected text                                 |
| ⌃ >      |                       |                                                                               |
| ⌘ (      | Decrease quote level  | Decrease the quote level of the selected text                                 |
| ⌃ <      |                       |                                                                               |

## Searching

| Shortcut | Action                 | Description                                                                                                  |
| :------: | --------------         | ----------------------------------------------------------------                                             |
| /        | Search in all messages | _Vim like_: Toolbar search (in all messages) -- see [official doc](http://manual.mailmate-app.com/view#search) |
| ⌥ ⌘ f    |                        | As above (`Edit ▸ Find ▸ Search All Messages...`)                                                            |
| ⌃ /      | Search in mailbox      | Advanced Search in the current mailbox                                                                       |
| ⌃ ⌥ ⌘ f  |                        | As above (`Edit ▸ Find ▸ Mailbox Search...`)                                                                |

## Navigation / View

| Shortcut | Action                  | Description                                                          |
| :------: | --------------          | ----------------------------------------------------------------     |
| o        | __O__pen                | Open message(s) in separate window(s)                                |
| e        | __E__xpand thread       | Expand selected threads                                              |
| E (⇧ e)  | Not __E__xpand thread   | Collapse selected threads                                            |
| l        | __L__ast thread message | Move to the last message of the current thread (expand it if needed) |
| n        | __N__ext thread         | Move to next thread / message                                        |
| p        | __P__revious thread     | Move to previous thread / message                                    |
| ↑        | Next message            | Move to the next message                                             |
| ↓        | Previous message        | Move to the previous message                                         |
| gg       | Select first message    | _Vim-like_: select first message from the current mailbox            |
| G        | Select last message     | _Vim-like_: select last message from the current mailbox             |
| L (⇧ l)  | __L__oad images once    | Load the embedded images (spam protection)                           |
| i        | Load __I__mages once    | As above                                                             |
|          |                         |                                                                      |

