# **StretchGPT: Expanded ChatGPT Conversations**

*Significantly enhances the ChatGPT UI for all screen sizes - without making any drastic changes to ChatGPT's base aesthetic.*

## [v4.0] 4 New Optional Features: Hide Avatars, Colored Message Indicators, Mobile Layout, Stacked/Centered Layout

> A bunch of awesome new UI enhancements are now available in the options menu!
>
> A few of these are now active by default, but they can be toggled on/off at any time. I have a feeling you'll wanna keep them on though ;)

1) **Hide avatars**
- Remove the avatars from the top left corner of every message, making the conversation window a lot more symmetrical and aesthetically pleasing, as well as freeing up a significant amount of horizontal space for text on smaller viewports.
2) **Customizable color indicators on user messages**
- Add a colored left border to all messages sent by you.
- Makes it super easy to distinguish your's vs. ChatGPT's messages, especially when "Hide avatars" is active.
- Choose from 27 different classy color presets in the dropdown list
  - A subtle 2-tone gradient is dynamically generated from the selected color, based on its lightness and saturation values.
  - My next update will include more color presets + the ability to set your own totally custom color values.
3) **Enable "mobile layout" on all screens**
 - Stacks the action buttons below the text in ChatGPT responses.
4) **Stacked message layout** - mobile only (<500px)
 - Centers all avatars and displays them in a separate row above the text in each message (ignored when avatars are visible)"

## [v3.0] - Sidebar/Chat History UI enhancements

> A toggleable set of sidebar/chat history menu tweaks now available in the UserStyle's config menu
1) Minor size reduction of fonts, icons and action buttons.
2) Slightly reduce the height of the selectable list items.
3) Improve chat title readability by:
  - Eliminating title truncation/ellipses.
  - Enabling text wrapping to make all the generated chat titles fully visible (no longer cut off after just a few words).
  - A couple subtle tweaks to some font weights and background/border colors in order to improve visual distinction between the different chat history "time period" sections ("Today", "Yesterday", "Previous 7 Days", etc.)

## [v1.0] - StretchGPT v1.0

**A simple, yet highly effective set of UI enhancements that significantly improve the readability and overall aesthetic of ChatGPT conversations on all screen sizes.**

### Core Feature:

Expands the total chat area by disabling the aggressive fixed width on the contents and replacing it with some responsive light padding that scales with your screen size (this padding only becomes noticeable on larger desktop screens)
  - @ 768px - the fixed max-width for conversation contents is disabled.
  - @ 1536px (Tailwind CSS's default "2xl" breakpoint) - some modest, responsive horizontal padding is introduced, ensuring optimal and consistent readability on all larger screens.
