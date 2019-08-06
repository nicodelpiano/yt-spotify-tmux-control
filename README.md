# yt-spotify-tmux-control

Simple scripts to allow you to have some control over Youtube and Spotify players.

## How to use

Place the scripts from the `scripts` folder into a local folder you feel comfortable executing stuff from `tmux.conf`: for this case I used `~`.

## Example

You can embed this functionality in Tmux providing your preferred bindings like this:

```
# Spotify control
bind N run-shell "~/spotify-control next"
bind C-p run-shell "~/spotify-control previous"
bind P run-shell "~/spotify-control playpause"

# Youtube control
bind . run-shell "~/yt-control"
```

and display info likewise:

```
set-option -g status-right "#[fg=black,bg=red] #(./yt-info) #[fg=black,bg=#1DB954] 🎧 #(./tmux-spotify-info)"
```

and it will look something like this:

![preview]()

## Caveats

- Just macOS support for now.

- For Youtube, recall that the script will take the first video in your tabs and only for `Google Chrome`.
