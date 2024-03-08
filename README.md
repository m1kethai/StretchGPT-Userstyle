# **StretchGPT**

**Userstyle to enhance the ChatGPT experience for both desktop and mobile browsers - by expanding the overall chat area and making a few subtle UI tweaks for improved aesthetics and conversation readability, all while respecting the original ChatGPT aesthetic. Plays nice with other userstyles/browser extensions and most features are toggleable.**

> Visit the main userstyle page for an easy 1-click installation:
>
> https://userstyles.world/style/9821/stretchgpt-extra-wide-chatgpt-conversations
---

### **Core Functionality:**

Widens the total chat area by disabling the (fairly aggressive) fixed width on the message contents and replacing it with responsive padding that scales according to whatever screen/window size you're using.

### **Additional/Toggleable Features:**
1. **Accent colors**
  - Pick one of the 30 custom color accent presets from the toolbar dropdown menu, to break up the monotonous default color palette and make it way easier to distinguish between your and ChatGPT's messages.
    - At the moment, this just changes the background color of your messages, the main prompt input field and a few other small elements - but a big update is currently in the works, that applies the accent color to several other key elements throughout the UI and includes a color picker to allow 100% user-customizable color schemes.
2. **Hidden avatars**
  - Remove the avatars from the top left corner of every message. Makes all the messages more symmetrical and aligned and frees up useful screen real estate, especially on smaller screens and mobile browsers.

---
### **Changelog:**

#### **[v5.0.3]**
- Bugfix [ChatGPT UI update]: custom color no longer applying to the prompt input field
- Cleaned up/replaced some outdated selectors to accommodate recent changes

#### **[v5.0.2]**
- Loosened up the horizontal message padding a bit
- Adjusted the BG color tint logic for improved contrast accessibility with more colors
- Removed "Mobile Layouts" + some other broken code/features

#### **[v5.0.1] Post UI-update hotfixes**
- A couple new fixes to restore the basic functionality after another big structural update by OpenAI a few days ago.
- Made a few tweaks to Accent Colors - added a few extra color presets and made a small fix to accommodate some elements in the new Custom GPT builder UI.
- Temporarily removed "Sidebar Tweaks" because it's been almost 100% unfunctional since the previous major UI overhaul. I'm currently working on a total overwork of this feature and it should be back in the next update.

#### **[v5.0.0] New "accent colors" feature + several fixes to accommodate the most recent major ChatGPT UI overhaul**
> *OpenAI's new UI revamp released today broke pretty much everything.. Everything should be good now though.*

I've also decided to release a new adaptive "accent colors" feature that I've been sitting on for a while. I'm flagging it as an experimental feature for now (turned off by default, of course) since I'm a huge stickler for accessibility and this isn't 100% color contrast accessible yet, given the large # of possible color options/combos, but I still think it's worth releasing to everyone in its current state, despite its imperfections.

I've had this feature permanently turned on for several months now and it's become a super essential part of my ChatGPT experience, livening everything up and making the default color palette feel so bland in comparison. It'll be getting lots of polishing and improving over the next few updates, so keep an eye out!

#### **[v4.0] 4 New Optional Features: Hide Avatars, Colored Message Indicators, Mobile Layout, Stacked/Centered Layout**
> **A bunch of nifty new UI enhancements are now available in the userstyle config!**
> *The subtlest new enhancements are set to active by default, but they can be easily toggled on/off at any time.*

  **Hide avatars**
- Remove the avatars from the top left corner of every message, making the conversation window a lot more symmetrical and aesthetically pleasing, as well as freeing up a significant amount of useful of horizontal space for text on smaller viewports.

**Customizable color indicators on user messages**
- Add a colored left border to all messages sent by you.
- Makes it super easy to distinguish your's vs. ChatGPT's messages, especially when "Hide avatars" is active.
- Choose from 27 different color presets in the dropdown list.
  - A subtle 2-tone gradient is dynamically generated from the selected color, based on its lightness and saturation values.
  - An upcoming update will include more color presets + the ability to define your own custom color values.

**"Mobile layout" on all screens**
 - Stacks the action buttons below the text in ChatGPT responses.

**Stacked message layout** (mobile-only - <500px viewport)
 - Centers all avatars and displays them in a separate row above the text in each message (ignored when avatars are visible)"

#### **[v3.0] Sidebar/Chat History UI enhancements**
> **Introducing an optional set of sidebar/chat history menu UI tweaks - toggleable options for these are now available in the userstyle config menu.**

- Minor size reduction of fonts, icons and action buttons.
- Slightly reduce the height of the selectable list items.
- Improve chat title readability by:
  - Eliminating title truncation/ellipses.
  - Enabling text wrapping to make all the generated chat titles fully visible (no longer cut off after just a few words).
  - A couple subtle tweaks to some font weights and background/border colors in order to improve visual distinction between the different chat history "time period" sections ("Today", "Yesterday", "Previous 7 Days", etc.).

#### **[v1.0] Core functionality**
- @ 768px viewport width, the fixed max-width for conversation contents is disabled.
- @ 1536px viewport width (Tailwind CSS's default "2xl" breakpoint), some modest, responsive horizontal padding is introduced, ensuring optimal and consistent readability on all larger screens.
