# System Architecture and Design Choices

## Example Flow:


- User 'A' creates a new document and initializes a new version control repository as the repository main author. The document is now tracked in the repository, and the intial version is saved as the first commit with a message, timestamp, and publish ID. 
- User 'A' updates the document's header, creates a draft, then commits the changes to the repository. The new version is saved as the most recent commit. The previous version is still available in the version history, accessible by the publish ID.
- User 'B' opens the same document and creates a draft branch. They make edits to the body, then submit the draft for review. The changes are saved as a new commit in the draft branch, with a message, timestamp, and publish ID.
- User 'A' reviews the changes made by User 'B'. Document differences are highlighted, and User 'A' either merges them into the main branch of the repository, or rejects the changes made. If merged, the new version is saved as the most recent commit in the main branch. If rejected, the draft remains on the draft branch, and the previous version remains as the most recent commit in the main branch.

## Data Models:

### Document:

### Version:

### User:

### Repository:
