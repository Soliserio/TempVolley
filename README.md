# TempVolley

A Windower addon for using supported temporary items, with up to three spaced attempts and checks for successful use.

## Supported Items

- Ontic Extremity
- Black Hourglass
- Obsidian Wing

## Installation

1. Extract the `tempvolley` folder into `Windower/addons/`.
2. Load the addon:

   `//lua load tempvolley`

To load automatically, add this line to `Windower/scripts/init.txt`:

`lua load tempvolley`

Loading the addon does not use an item.

## Commands

| Command | Action |
|---|---|
| `//tempvolley start ontic` | Use Ontic Extremity |
| `//tempvolley start hourglass` | Use Black Hourglass |
| `//tempvolley start wing` | Use Obsidian Wing |
| `//tempvolley start` | Use Ontic Extremity by default |
| `//tempvolley cancel` | Cancel the current request |

## Multiple Characters

With Windower's Send addon, send a request to all connected local clients:

`//send @all tempvolley start ontic`

Replace `ontic` with `hourglass` or `wing` for the other items.

TempVolley must be loaded on every participating client. Each character checks its own temporary inventory and handles its own attempts.

To cancel across connected clients:

`//send @all tempvolley cancel`

## Timing and Checks

- Waits three seconds before the first attempt.
- Allows up to three attempts, spaced twenty seconds apart.
- Searches temporary inventory only.
- Requires the character to be idle with menus closed.
- Stops when use is confirmed, the item is no longer available, the character zones or logs out, or the request times out.
- Requests have a ninety-second timeout.

Cancellation cannot undo an item action already sent to the game.

## Keyboard Shortcuts

Custom keyboard shortcuts are optional and are not included. Bind your preferred keys to the commands above using your own hotkey setup.

## Updating

Replace the addon files, then reload:

`//lua reload tempvolley`

## Testing Status

Ontic Extremity has been tested successfully in game. Black Hourglass and Obsidian Wing have passed offline checks but still require live validation.

**Author: Soliserio**
