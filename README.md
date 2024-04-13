# rem

"rem" is a Bash application for creating reminders on Linux systems. It utilizes the `at` command to schedule system notifications with custom messages at specified times and `notify-send` to deliver such reminders. With its minimalist design and straightforward syntax, "rem" aims to provide users with a seamless experience for managing reminders effortlessly.

## Features

- Schedule reminders with custom messages using a simple syntax.
- Utilizes the `at` command for scheduling, ensuring compatibility with most Linux distributions.
- Lightweight and easy to use, perfect for users seeking a streamlined reminder solution.

## Usage

```bash
$ rem your reminder message | at [time]
```

### Examples

```bash
$ rem Buy the milk | at 6pm
$ rem Take out the trash | at 8pm Tomorrow
```

**First Bonus**

Set an alias in your `.bashr`|`.zshrc`|`.fishrc` like `alias in="at now +"`, so that you can also write

```bash
$ rem Call mom | in 45 minutes
```

instead than
```bash
rem Call mom | at now + 45 minutes
```

## Installation

1. Click on the "Code" button.
2. Select "Download ZIP" to download the repository as a ZIP file.
3. Extract the `rem` script from the downloaded ZIP file.
4. Make the rem script executable:
    ```bash
    $ chmod +x rem
    ```

**Second bonus**

Move the script in a location under your `$PATH` (e.g. `$HOME/.local/bin` ) so that it can be executed everywhere in your system.

