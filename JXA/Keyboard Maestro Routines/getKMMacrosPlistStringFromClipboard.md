
```js
ObjC.import('AppKit');

// Returns a string containing the "source code" (aka plist) of the Keyboard
// Maestro Macro(s) on the clipboard, if any, otherwise returns undefined.
// PARAMETERS:
//   types  OPTIONAL. You can pass the available clipboard types, usually
//          retrieved from getClipboardTypes(), if you want. You would do
//          this if you had already called getClipboardTypes() for some
//          other reason, and wanted to eliminate calling it again. No big
//          deal either way.
// UPDATED: 2016/07/05 08:44 PDT
function getKMMacrosPlistStringFromClipboard(types) {
	return ClipboardUtils.getClipboardStringForType(kmConstants.macrosClipboardType, types);
}
```

Uses:
* [ClipboardUtils](..%2FClipboardUtils.md)
* [kmConstants](kmConstants.md)

## For a complete example, see:
* [DEMO - Clipboard Read, Write, and KM Action/Macro Plist example](DEMO%20-%20Clipboard%20Read%2C%20Write%2C%20and%20KM%20Action%20and%20Macro%20Plist%20example.md)