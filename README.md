# Swift UI Testing Demo

UIKit sample project focused on UI test structure, reusable test operations, and behavior checks around a small navigation flow.

The repo demonstrates how to keep UI automation code readable by extracting shared interactions into operation helpers instead of writing every assertion inline in the test body.

## What This Project Shows

- XCUITest target with launch and interaction tests.
- Reusable operation objects under `UITestUITests/Operation.swift`.
- Example app screens built with UIKit/storyboards.
- Quick/Nimble dependency setup through Carthage.
- A simple MVVM-style view model used by the demo app.

## Main Modules

| Path | Responsibility |
| --- | --- |
| `UITest` | Demo iOS application |
| `UITest/ViewModel.swift` | Small state holder for the demo UI |
| `UITestUITests` | UI automation target |
| `UITestUITests/Operation.swift` | Shared UI test interactions |
| `Cartfile` | Quick/Nimble dependency declaration |

## Running

```sh
carthage bootstrap --platform iOS
open UITest.xcodeproj
```

Select the `UITest` scheme and run tests from Xcode.

## Technical Notes

- Keep UI queries and repeated actions in operation helpers.
- Keep test methods focused on scenario intent and assertions.
- Prefer accessibility identifiers for stable UI tests when extending this sample.
- If moving this to a modern codebase, Swift Package Manager would be a cleaner dependency path than Carthage.

## Author

Dambert Muñoz

Email: [dmsantillana2705@gmail.com](mailto:dmsantillana2705@gmail.com)
