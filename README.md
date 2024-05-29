# rem

`rem` is a Bash script designed to create reminders on Linux systems. It leverages the `at` command to schedule notifications with custom messages at specified times, uses `notify-send` to display these reminders, and `paplay` to emit a notification sound. With its minimalist design and straightforward syntax, `rem` offers users an easy and efficient way to manage their reminders.

## Features

- Schedule reminders with custom messages using a simple syntax.
- Lightweight and easy to use, perfect for users seeking a streamlined reminder solution.

## Usage

```bash
rem help   
Usage: rem <message> at:<time>  # add new reminder AT given time (e.g. 16:00)
       rem <message> in:<time>  # add new reminder IN given time (e.g. 5 min, 1 hour)
       rem                      # list all reminders and their ID
       rem del <id>             # delete reminder with <id>
       help                     # to show this message
```

### Examples

```bash
$ rem Buy the milk at:6pm Tomorrow
$ rem Take out the trash in:30 min
```

Calling `rem` without arguments will show the existing reminders with execution time, time left and the reminder ID.

```bash
$ rem
- Apr/13/2024 17:39/0h:28m (6) call mom
- Apr/13/2024 18:00/0h:49m (4) buy the milk
- Apr/14/2024 20:00/01d (5) take out the trash
```

The ID is important to cancel a reminder.

```bash
$ rem del 4                           
removing reminder 4:"buy the milk" from the queue
Continue? [ENTER/Ctrl-C]

done
$ rem
- Apr/13/2024 17:39/0h:27m (6) call mom
- Apr/14/2024 20:00/01d (5) take out the trash
```


## Installation

1. Click on the "Code" button.
2. Select "Download ZIP" to download the repository as a ZIP file.
3. Extract the `rem` script from the downloaded ZIP file.
4. Make the rem script executable:
    ```bash
    $ chmod +x rem
    ```

Move the script in a location under your `$PATH` (e.g. `$HOME/.local/bin` ) so that it can be executed everywhere in your system.


