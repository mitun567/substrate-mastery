# Unblocking Cargo Process

When encountering a `Blocking waiting for file lock on package cache` error in Cargo, you can unblock the process by following these steps:

## Step 1: Remove the Lock File
Run the following command to remove the `.package-cache` lock file:

```bash
rm -f ~/.cargo/.package-cache
```

This will delete the lock file that might be causing the blockage.

## Step 2: Retry Your Cargo Command
After removing the lock file, retry your command. For example:

```bash
cargo build --release
```

This should resolve the issue and allow the Cargo process to proceed.
