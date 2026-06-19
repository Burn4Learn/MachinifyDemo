A (kind of silly) demo project that manages an IMDB watch list, keeping it in sync with an excel spreadsheet. 

Highlights:

  - API call to the automation folder, in orchestrator, to retrieve all assets and place into two dictionaries; 
    1) Credentials (with secure passwords)
    2) Config (containing all asset objects, which must be cast unfortunately, but....you get one, passable object to all flows, with one read)
  - Fairly robust error catching, given the time constraints (all blocks use try/catch)
 - Decently segmented/reusable components, again, given time constraints. Admittedly, the editList xaml uses a lot of element finders. I would refactor this to use fewer, and also segment the lift a little more
  - Cleanup. Gracefully close applications, alert users (will alert using SMTP messaging if time permits)
  - Would refactor Excel flows to use the same "consumer" of the Excel app, and break the verbs into flows (So a top level "accessor" xaml, and then child xaml files that read, write, etc)

Growth Edges for me, highlighted in this project:

  - using the object repository. at the time (7/2025), wasn't so familiar. Should re-write to use, now. (6/2026)
  - testing and mocking data. Not familiar with mocking data for UiPath, but would like to learn/implement as my next project. Am familiar with building out a test suite, however. 
