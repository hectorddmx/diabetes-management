# Blood glucose management app

## Introduction
Welcome to Distillery!

For the next week you'll build an iOS application from scratch to handle blood glucose levels.
This task is to measure your current skills and your growth level.

## Features

The application will consist of the following features:
- Login.
- See blood glucose level records in a graph.
- Create new glucose level records.

## Criteria

We want you to develop the app using this tools and techniques:
I separate those we want as required and some that are optional.

### Required requirements

- Use Git along the way
	- Fork this repo.
	- Use feature branches.
		- https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
	- Create pull requests for code review targetting your own repo.
		- Guide: https://guides.github.com/activities/hello-world/#pr

- Use TDD (Test Driven Development)
	- Develop completely the application using TDD.
	- You'll require to have good code coverage.
	- Guide: https://qualitycoding.org/ios-tdd/
	- Guide: https://mokacoding.com/blog/step-by-step-tdd-in-swift-part-1/
	- Video series guide: https://www.essentialdeveloper.com/professional-ios-engineering-series.

- Use MVVM-C (Model-View-ViewModel-Coordinator (MVVM-C))
	- For the binding use closures or combine.
	- Example: https://marcosantadev.com/mvvmc-with-swift/.

- Use DI (Dependency Injection)
	- Guide:  https://www.essentialdeveloper.com/articles/s03e05-dependency-injection-patterns-applied-in-ios-apps-professional-ios-engineering-series

- UI as code (programmatic UI)
	- Don't use storyboards
	- Don't use xib's/nib's
	- Use UIKit. 
	- SwiftUI can be used but only for individual views.
		- Guide: https://sarunw.com/posts/swiftui-in-uikit/
	- Only write the UI as code.
		- For UIKit, override [loadView() from UIViewController](https://developer.apple.com/documentation/uikit/uiviewcontroller/1621454-loadview)
		- Guide: https://swiftrocks.com/writing-cleaner-view-code-by-overriding-loadview

- Autolayout
	- Don't use a library like cartography or snapkit to abstract autolayout constraints. 
	- Use autolayout and autolayout anchors instead.
		- Guide: https://www.hackingwithswift.com/read/6/5/auto-layout-anchors

- Network layer
	- Don't use a dependency for handling network requests (Alamofire, Moya, etc)
	- Use URLSession directly

- Models
	- Don't use a dependency for parsing JSON (SwiftyJSON, ObjectMapper, Mantle, etc)
	- Use Codable/Encodable/Decodable protocols
		- Guide: https://www.hackingwithswift.com/articles/119/codable-cheat-sheet

- Graphs
	- Use the dependency Charts: https://github.com/danielgindi/Charts

- Dependencies
	- Use SwiftPM for any dependency that's mentioned here or that are not disallowed.

### Optional requirements
- Commits
	- Use semantic/conventional commits: https://www.conventionalcommits.org/en/v1.0.0-beta.2/#summary

- Do UI testing and snapshot testing
	- For screens and UI components take snapshots and compare them
	- Use pointfreeco library: https://github.com/pointfreeco/swift-snapshot-testing
	- Guide: https://medium.com/dev-jam/snapshot-testing-in-swift-9d52cbec075c

- CI, use Github Actions
	- https://github.com/Apple-Actions
	- https://docs.github.com/en/actions/guides/building-and-testing-swift

- Deployment and QA
	- Use external testflight testing with shareable URL.
	- Don't push to the App Store.
	- Use semantic versioning

- Static Analysis:
	- Use SwiftLint: https://github.com/realm/SwiftLint
		- Rules: https://github.com/aws-amplify/amplify-ios/blob/main/.swiftlint.yml
	- Use SwiftFormat: https://github.com/nicklockwood/SwiftFormat
		- Rules: https://github.com/aws-amplify/amplify-ios/blob/main/.swiftformat

## User stories

### Login page

[[GM1 - Login]]
> As a user I want to be able to use my password I've created in the [jade sign up page](https://app.jadediabetes.com/signup.html) and on success, get redirected to the home page. 

[[GM2 - Login error]] 
> As a user I would like to know that I've added an incorrect email and password. 
		
### Home page 
[[GM3 - Home page with glucose records]]
> As a user, I want to see my previously recorded blood glucose values in a bubbleChart, displayed in `mmol/L` over time `days`

[[GM4 - Add blood glucose record in a modal]]
> As a user, I want to be able to open a modal page where I can record new blood glucose values


## API

The API that handle the login, recording the values and displaying the values is the Jade API. Please read the [[API introduction]] to understand how to use the API.