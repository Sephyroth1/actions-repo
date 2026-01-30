# action-repo

This repository is used to trigger GitHub webhook events for the assessment task.

## Purpose

The repository is configured to send GitHub webhook events to an external webhook
endpoint on the following actions:

- Push
- Pull Request
- Merge (via merged pull requests)

<<<<<<< HEAD
1. Fork this repository.
2. Create a new workflow file in your repository.
3. Copy and paste the desired workflow from this repository into your new workflow file.
4. Customize the workflow as needed.
5. Commit and push your changes.

## Contributing

If you have any suggestions or improvements for these workflows, feel free to open an issue or submit a pull request.
=======
These events are sent to the webhook server implemented in the `webhook-repo`.

## Configuration

A GitHub webhook is configured in this repository:

- Payload URL: `<ngrok-url>/webhook`
- Content type: `application/json`
- Events:
  - Push
  - Pull requests

## How It Is Used

This repository itself does not contain application logic.
It is used only to generate GitHub events such as:

1. Pushing commits
2. Creating pull requests
3. Merging pull requests

These actions trigger webhook calls that are processed by the backend in
`webhook-repo`.

## Testing

To test the system:

1. Push a commit to this repository
2. Create a pull request
3. Merge the pull request

Each action should appear in the UI provided by the `webhook-repo`.
>>>>>>> 2e8fb857a326fb7c893dc331ee37ca4837e5e9e9
