# StretchGPT Userstyle Development Guide

**StretchGPT is a CSS userstyle that enhances ChatGPT's UI by expanding the chat area, adding color customization, and providing various toggleable features. It uses LESS preprocessing and is distributed via browser extension platforms.**

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Bootstrap and Setup
- Clone the repository - no additional dependencies or build tools required
- Install development tools for validation:
  ```bash
  npm install -g less
  npm install --save-dev stylelint stylelint-config-standard postcss-less
  ```
- Verify LESS compiler: `lessc --version` (should show v4.4.0+)

### Build and Validation Process
- **NEVER CANCEL builds or validation** - LESS compilation takes ~0.17 seconds
- **Primary validation command**:
  ```bash
  npm run validate
  ```
  - Runs LESS compilation test (~0.17 seconds)
  - Validates CSS syntax with userstyle variables
  - **NEVER CANCEL** - Set timeout to 30+ seconds minimum
- **Individual validation commands**:
  ```bash
  npm run compile-test  # LESS compilation validation (~0.17 seconds)
  npm run lint          # Basic syntax check (informational only)
  ```

### Manual Testing and Installation
- **CRITICAL**: Always test changes manually in browser after modifications
- Install browser extension: Stylus (recommended) or Stylish
- **Installation methods**:
  1. **Production**: Install from https://userstyles.world/style/9821/stretchgpt-extra-wide-chatgpt-conversations
  2. **Development**: Open `StretchGPT.userstyle.css` in browser with Stylus extension installed
- **Manual testing time**: Allow 20-30 minutes for complete validation including setup

### Test Scenarios (ALWAYS run these after changes)
1. **Basic Installation** (5 minutes):
   - Navigate to https://chatgpt.com
   - Verify chat area is wider than default
   - Confirm Stylus shows style is active
2. **Stretch Factor Testing** (5 minutes):
   - Open Stylus settings for StretchGPT
   - Test all stretch factor options (Conservative, Roomy, Spacious, Unrestricted)
   - Verify chat width changes appropriately
3. **Color Customization** (5 minutes):
   - Enable color customization features
   - Test different color presets
   - Send test message to verify colors apply
4. **Responsive Design** (5 minutes):
   - Resize browser to different widths
   - Test mobile viewport (<768px)
   - Verify layout remains functional

## File Structure and Key Components

### Repository Root
```
.
├── StretchGPT.userstyle.css    # Main userstyle file (300 lines)
├── README.md                   # User documentation
├── USW-README.md               # UserstStyles.world documentation  
├── CHANGELOG.md                # Version history
├── LICENSE                     # License file
├── .gitignore                  # Git ignore rules
└── package.json                # Development tools (dev-only)
```

### Main File: StretchGPT.userstyle.css
- **Lines 1-89**: UserStyle metadata headers with @var declarations
- **Lines 90-300**: LESS code with CSS selectors and styling
- **Key @var variables**:
  - `@stretchFactor`: Main width control (0-4)
  - `@enableColorization`: Master color toggle
  - `@colorPreset`: Color selection (~70 options)
  - `@enableChatBubbleStretch`: Bubble expansion toggle
  - `@hideDisclaimer`: Footer disclaimer toggle

## Common Development Tasks

### Making CSS/Style Changes
1. **ALWAYS validate first**: `npm run validate` (~0.17 seconds)
2. Edit `StretchGPT.userstyle.css` directly
3. **Re-validate immediately**: `npm run validate` 
4. **Manual browser testing required** - install and test in browser
5. Test all scenarios listed above (20-30 minutes total)

### Adding New Features
1. Add new @var declaration in metadata header (lines 8-89)
2. Implement LESS logic in main code section (lines 90-300)
3. **CRITICAL**: Validate LESS compilation with new variables
4. **ALWAYS test manually** in browser with all scenarios

### Debugging Style Issues
1. Check LESS compilation: `npm run compile-test`
2. Install in browser for live testing
3. Use browser DevTools to inspect CSS application
4. Check ChatGPT DOM structure (selectors may change with OpenAI updates)
5. Verify across different viewport sizes

### Version Management
1. Update version in UserStyle header (line 3)
2. Add entry to CHANGELOG.md
3. Test installation from file before publishing
4. **NEVER skip manual browser validation**

## Validation Requirements

### Pre-commit Checklist
- [ ] `npm run validate` passes (~0.17 seconds - **NEVER CANCEL**)
- [ ] Manual browser installation works
- [ ] All 4 test scenarios completed (20-30 minutes)
- [ ] No JavaScript errors in browser console
- [ ] ChatGPT functionality remains intact
- [ ] Style works on mobile and desktop viewports

### Expected Timing
- **LESS compilation**: ~0.17 seconds (**NEVER CANCEL** - set 30+ second timeout)
- **Complete validation**: 20-30 minutes including manual testing
- **Browser installation**: 2-3 minutes
- **Single test scenario**: 5 minutes each

## Troubleshooting

### Common Issues
1. **LESS compilation fails**: Check @var declarations match usage in code
2. **Style not applying**: Verify Stylus extension is active and userstyle is enabled
3. **Layout breaks**: Test responsive design across different viewport sizes
4. **Colors not working**: Check @enableColorization is enabled in browser

### Development Tools Issues
- CSS linting is disabled due to LESS preprocessing complexity
- Use `npm run compile-test` for syntax validation instead
- Manual browser testing is the primary validation method

### ChatGPT UI Changes
- OpenAI frequently updates ChatGPT's DOM structure
- Selectors in CSS may need updates after ChatGPT releases
- Always verify functionality after OpenAI updates
- Check GitHub issues for reports of broken functionality

## Critical Reminders
- **NEVER CANCEL** any validation commands - they complete in under 1 second
- **ALWAYS test manually** in browser after any changes
- **Complete validation requires 20-30 minutes** including manual testing
- **Set timeouts of 30+ seconds** for validation commands to prevent premature cancellation
- **Manual testing is mandatory** - CSS-only changes still require browser verification