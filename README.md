# **StretchGPT**

**Userstyle to enhance the ChatGPT experience for both desktop and mobile browsers - by expanding the overall chat area and making a few subtle UI tweaks for improved aesthetics and conversation readability, all while respecting the original ChatGPT aesthetic. Plays nice with other userstyles/browser extensions and most features are toggleable.**

> Visit the userstyles.world page for an easy 1-click installation:
>
> https://userstyles.world/style/9821/stretchgpt-extra-wide-chatgpt-conversations
---

### **Core Functionality:**

Expands the usable chat area by >200% by replacing the default restrictive max-width and fixed margins/padding with much more subtle, adaptive spacing that scales according to your current viewport size.

### **Extra/Optional Features:**

1. **Accent Colors**
  - Pick from the 40+ included color presets to liven up the dull default color palette and make it easier to distinguish between your prompts and ChatGPT's responses.
  - There are separate toggles in the userstyle's dropdown menu to apply the selected color to your messages and/or your message bubbles, as well as the prompt input elements.
2. **Hide Avatars**
  - Remove the avatars from ChatGPT responses and free up more screen real estate (makes the most significant difference in mobile and tablet browsers).
3. **Hide Disclaimer Message**
---
> The previous features below recently broke due to a few big ChatGPT UI updates and have been removed for the time being, but I'm currently working on fixes for them and will be re-integrating them soon:

- Resizeable prompt input/textarea
- Colorpicker
- Expanded sidebar menu
- Accent colors for header and sidebar elements
- Configurable padding/width for the main chat content 
---
### **Changelog:**

#### **[6.0]**
- Fixed all the broken things for both desktop and mobile VPs
- Added some more cool custom color presets
- Added some new color customization options (you can now apply the color to just your message bubble or the bubble + full chat item/row. 
#### **[5.1]**
- Bugfix (ChatGPT update) - custom color no longer applying to the prompt input field
- Colorize feature now fully working and enabled for "Light" ChatGPT theme
- Added an accessible text mixin to ensure that the text is always readable against any custom background color
- Split custom color options into two separate ones (user message BG and input/textarea BG)
- Cleaned up/replaced some outdated selectors to accommodate recent changes

#### **[5.0.2]**
- Loosened up the horizontal message padding a bit
- Adjusted the BG color tint logic for improved contrast accessibility with more colors
- Removed "Mobile Layouts" + some other broken code/features

#### **[5.0.1] Post UI-update hotfixes**
- A couple new fixes to restore the basic functionality after another big structural update by OpenAI a few days ago.
- Made a few tweaks to Accent Colors - added a few extra color presets and made a small fix to accommodate some elements in the new Custom GPT builder UI.
- Temporarily removed "Sidebar Tweaks" because it's been almost 100% unfunctional since the previous major UI overhaul. I'm currently working on a total overwork of this feature and it should be back in the next update.

#### **[5.0.0] New "accent colors" feature + several fixes to accommodate the most recent major ChatGPT UI overhaul**
> *OpenAI's new UI revamp released today broke pretty much everything.. Everything should be good now though.*

I've also decided to release a new adaptive "accent colors" feature that I've been sitting on for a while. I'm flagging it as an experimental feature for now (turned off by default, of course) since I'm a huge stickler for accessibility and this isn't 100% color contrast accessible yet, given the large # of possible color options/combos, but I still think it's worth releasing to everyone in its current state, despite its imperfections.

I've had this feature permanently turned on for several months now and it's become a super essential part of my ChatGPT experience, livening everything up and making the default color palette feel so bland in comparison. It'll be getting lots of polishing and improving over the next few updates, so keep an eye out!

#### **[4.0] 4 New Optional Features: Hide Avatars, Colored Message Indicators, Mobile Layout, Stacked/Centered Layout**
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

#### **[3.0] Sidebar/Chat History UI enhancements**
> **Introducing an optional set of sidebar/chat history menu UI tweaks - toggleable options for these are now available in the userstyle config menu.**

- Minor size reduction of fonts, icons and action buttons.
- Slightly reduce the height of the selectable list items.
- Improve chat title readability by:
  - Eliminating title truncation/ellipses.
  - Enabling text wrapping to make all the generated chat titles fully visible (no longer cut off after just a few words).
  - A couple subtle tweaks to some font weights and background/border colors in order to improve visual distinction between the different chat history "time period" sections ("Today", "Yesterday", "Previous 7 Days", etc.).

#### **[1.0] Core functionality**
- @ 768px viewport width, the fixed max-width for conversation contents is disabled.
- @ 1536px viewport width (Tailwind CSS's default "2xl" breakpoint), some modest, responsive horizontal padding is introduced, ensuring optimal and consistent readability on all larger screens.
