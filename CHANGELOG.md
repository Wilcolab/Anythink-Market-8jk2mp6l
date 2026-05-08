# Changelog

## [Unreleased]

### Added
- **Exponentiation operator (^)** - Added support for power function calculations
  - Added `^` button to calculator UI
  - Implemented `power` operation in server-side controller using `Math.pow()`
  - Added keyboard support for `^` key
  
### Changed
- Updated `calculate()` function in `client.js` to handle the power operator
- Extended keyboard event listener regex pattern to recognize `^` operator
- Added `power` operation to operations object in `api/controller.js`

### Files Modified
- `public/index.html` - Added power operator button
- `public/client.js` - Added power case to switch statement and updated keyboard regex
- `api/controller.js` - Added power function to operations object

### Implementation Details
- **Client-side (client.js)**:
  - Maps `^` operator to `?operation=power` query parameter
  - Keyboard support: Users can now press `^` to perform exponentiation
  
- **Server-side (controller.js)**:
  - Power operation uses `Math.pow(operand1, operand2)`
  - Follows existing validation patterns for operands

@@### Testing
@@- No new tests added yet - existing validation tests continue to apply
@@- Manual testing required for edge cases (negative bases, fractional exponents, etc.)
@@
@@## [Unreleased v2.0] - Enhanced Operations and UI
@@
@@### Added
@@- **Square Root (√)** - Client-side calculation using `Math.sqrt()`
@@  - Direct computation without server call
@@  - Error handling for negative numbers
@@  
@@- **Modulo operator (%)** - Remainder calculation
@@  - Server-side operation for consistency
@@  - Added to keyboard support (% key)
@@  
@@- **Improved UI/UX**:
@@  - Rounded corners on buttons (`border-radius: 6px`)
@@  - Color-coded buttons: Green for operations, Blue for control buttons
@@  - Smooth hover effects with lift animation
@@  - Better visual feedback on button interaction
@@  - Reorganized button layout with logical grouping (advanced ops row, numbers rows)
@@  - Improved button spacing and borders for cleaner appearance
@@  
@@- **Enhanced Keyboard Support**:
@@  - Added `%` key for modulo operation
@@  - Added `Enter` key as alternative to `=`
@@  
@@### Files Enhanced
@@- `public/index.html` - Reorganized button layout with comments, added √ and % buttons
@@- `public/client.js` - Added `sqrtPressed()` function, updated switch statement and keyboard listener
@@- `api/controller.js` - Added modulo operation
@@- `public/default.css` - Enhanced button styling with colors, hover effects, active states
@@
@@---
@@
@@## [1.0] - 2023-06-15

### Initial Release
- Basic arithmetic operations (add, subtract, multiply, divide)
- Calculator UI with number buttons and operations
- REST API backend with Express.js
- Test suite with Mocha and Chai
