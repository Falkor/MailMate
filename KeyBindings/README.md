-*- mode: markdown; mode: visual-line; fill-column: 80 -*-
`README.md`

Copyright (c) 2015 [Sebastien Varrette](mailto:<Sebastien.Varrette@uni.lu>)

      Time-stamp: <Wed 2015-11-11 22:28 svarrette>

------------------------------
# Falkor MailMate KeyBindings

* [Reference Documentation](http://manual.mailmate-app.com/custom_key_bindings)
* [List of Key Binding Selectors](http://manual.mailmate-app.com/key_binding_selectors)


Once of the killing feature of [MailMate](http://mailmate-app.com) is the complete freedom left to configure [custom key bindings](http://manual.mailmate-app.com/custom_key_bindings).
You can configure the `Falkor` key-bindings by placing the file [`Falkor.plist`](Falkor.plist) in:

```sh
~/Library/Application Support/MailMate/Resources/KeyBindings
```

Then relaunch [MailMate](http://mailmate-app.com) and set the shortcut in the preferences pane (`MailMate ▸ Preferences... ▸ General ▸ Custom Key Bindings ▸ Enable`). Enable the key bindings that you want by entering them in the box below, e.g. `Falkor`.

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

## General Actions 

| Shortcut | Action         | Description                                                      |
| :------: | -------------- | ---------------------------------------------------------------- |
| ⌘ ↩      | Send message   | After composing your message, use this combination to send it.   |
| z        | Undo           | Undo the last action (moved messages or keyword changes)         |
| Z (⇧ z)  | Redo           | Redo action (moved messages or keyword changes)                  |
| ⌃ s      | __S__ave       | Save the current message in the `Drafts` mailbox                 |
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

| Shortcut | Action                 | Description                                                                                                            |
| :------: | --------------         | ----------------------------------------------------------------                                                       |
| /        | Search in all messages | _Vim like_: Toolbar search (in all messages) -- see [official doc](http://manual.mailmate-app.com/view#search) (⌥ ⌘ f) |
| ⌃ /      | Search in mailbox      | Advanced Search in the current mailbox  -- see [official doc](http://manual.mailmate-app.com/view#search) (⌃ ⌥ ⌘ f)    |
|          |                        |                                                                                                                        |

_**Note:**_ searching in all message allow you to benefit from the flexible [search specifications](http://manual.mailmate-app.com/view#search) available in [MailMate](http://mailmate-app.com). 
For instance typing:

```txt
foo f !smith t (smith or joe)
```

is understood as 

```txt
Message contains "foo" and From does not contain "smith" and (To contains "smith" or "joe")
```

Currently supported modifiers:

| Modifier | Search scope                     |
|----------|----------------------------------|
| f        | From                             |
| s        | Subject                          |
| t        | To (Recipients)                  |
| a        | Any address header               |
| b        | Body text (unquoted body text)   |
| q        | Quoted text                      |
| m        | Message (Common Headers or Body) |
| T        | Tags                             |


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

## Filtering

| Shortcut | Action                    | Description                                                                                           |
| :------: | --------------            | ----------------------------------------------------------------                                      |
| j        | __J__unk                  | Move selected message(s) to Junk                                                                      |
| J (⇧ j)  | Not __J__unk              | Mark as NOT junk and move the message to `INBOX`                                                      |
| !        | Important / Urgent        | Flag the message as (important/urgent)                                                                |
| -        | Toggle the Mute state     | Archives the conversation, and all future messages skip the Inbox unless sent or cc'd directly to you |
| A (⇧ a)  | __A__rchive               | move the message(s) to the `Archive` mailbox                                                          |
| x        | Delete                    | Delete the message(s)                                                                                 |
| X (⇧ x)  | Delete thread             | Delete the complete Thread                                                                            |
| u        | Toggle [__U__n]read state | Mark the message(s) as read/unread                                                                    |
| m        | __M__ove to mailbox       | Move the message(s) to a Mailbox to select from a searchable list                                     |
| C (⇧ c)  | __C__orrespondence        | Show the messages having the same correspondent(s)                                                    |
| D (⇧ d)  | __D__ownload              | Download the attachment in the default Download folder (`~/Download/`)                                |
|          |                           |                                                                                                       |

## Selection / Combo keys `*`

| Shortcut   | Action                       | Description                                               |
| :------:   | --------------               | --------------------------------------------------------- |
| ⌃ a        | Select __A__ll               | Select all messages of the current mailbox                |
| *a         |                              | As above                                                  |
| *n         | __N__ot Select All           | De-select   all messages of the current mailbox           |
| *r         | Select __R__ead              | Select all messages you've read.                          |
| *u         | Select __U__nread            | Selects all unread mail.                                  |
| *f         | Select __F__lagged / starred | Selects all flagged / starred / important / urgent  mail. |
| *!         |                              | As above                                                  |
| *F (* ⇧ f) | Select Not flagged           | Selects all unflagges / unstarred mail.                   |
|            |                              |                                                           |

## Tags

I bind the default shortcut to add tags to `⇧ t` in the `Tags ▸ Tags editor shortcut`, which let the `t` key able to initiate a combo on tags as follows: 

| Shortcut | Action                  | Description                                    |
| :------: | --------------          | ---------------------------------------------- |
| te       | __T__ag __E__xpectReply | Toggle the tag `ExpectReply` to the message(s) |
| td       | __T__ag __D__elegated   | Toggle the tag `Delegated` to the message(s)   |
|          |                         |                                                |

## GoTo Mailbox

All `GoToMailbox` actions are prefixed by `g`.

If you wish to configure a shortcut to access a given smart mailbox, obtain its UUID from

```sh
~/Library/Application\ Support/MailMate/Mailboxes.plist
```

| Shortcut   | Action                | Description                                                                                                                      |
| :------:   | --------------        | ---------------------------------------                                                                                          |
| ga         | Go to __A__ll         | Go to the `All Messages` Smart Mailbox                                                                                           |
| gA (g ⇧ a) | Go to __A__rchives    | Go to the `Archives` Mailbox                                                                                                     |
| gd         | Go to __D__elegated   | Go to the `Delegated` Mailbox                                                                                                    |
| gf         | Go to __F__lagged     | Go to the `Flagged` Smart Mailbox (hosting Important/Urgent messages)                                                            |
| g!         |                       | As above                                                                                                                         |
| gD (g ⇧ d) | Go to __D__rafts      | Go to the `Draft` Mailbox                                                                                                        |
| gl         | __L__ist Mailbox      | Show mailbox selection window                                                                                                    |
| gi         | Go to __I__NBOX       | Go to the `INBOX` Mailbox                                                                                                        |
| gs         | Go to __S__end        | Go to the `Send` Mailbox                                                                                                         |
| gu         | Go to __U__nread      | Go to the `Unread` Smart Mailbox                                                                                                 |
| ge         | Go to __E__xpectReply | Go to the `Expect a Reply` Smart Mailbox -- see [this blog post](http://jeremy.cowgar.com/2014/09/18/mailmate-waiting-on-reply/) |
| gj         | Go to __J__unk        | Go to the `Junk` Smart Mailbox                                                                                                   |
| gv         | Go to __V__IPs        | Go to the `VIPs` Smart Mailbox                                                                                                   |
|            |                       |                                                                                                                                  |
