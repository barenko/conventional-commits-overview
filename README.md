# This project was generated using the following script

    # Initialize a new Git repository
    git init

    # Create an empty commit using the Conventional Commit convention
    git commit --allow-empty -m "chore: Initial commit"

    # Create empty commits with different types and scopes
    git commit --allow-empty -m "feat(auth): Add authentication"
    git commit --allow-empty -m "fix(ui): Fix styling issue"
    git commit --allow-empty -m "docs(readme): Update README"
    git commit --allow-empty -m "refactor(api): Refactor API endpoints"

    # Create empty commits with breaking changes
    git commit --allow-empty -m "feat(api): Add new endpoint\n\nBREAKING CHANGE: The existing API is no longer compatible."

    # Create empty commits for infrastructure changes
    git commit --allow-empty -m "ci: Set up continuous integration"
    git commit --allow-empty -m "build(docker): Create Dockerfile"
    git commit --allow-empty -m "test(unit): Add unit tests"

    # Create empty commits for branch/merge operations
    git checkout -b feature/new-feature
    git commit --allow-empty -m "feat: Implement new feature"
    git checkout main
    git merge --no-ff feature/new-feature -m "Merge branch 'feature/new-feature'"

    # View the commit history
    git log


    # Install cargo
    # https://doc.rust-lang.org/cargo/getting-started/installation.html
    curl https://sh.rustup.rs -sSf | sh

    # Install git-cliff
    cargo install git-cliff

    # Configure git-cliff
    git cliff --init

    # Generate the changelog
    git cliff -o CHANGELOG.md

    # View the generated changelog
    cat CHANGELOG.md
