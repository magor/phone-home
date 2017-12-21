# secure-tunnel
reverse ssh proxy to allow connecting to machine behind nat via server

Inspired by https://blog.kylemanna.com/linux/ssh-reverse-tunnel-on-linux-with-systemd/ and https://gist.github.com/drmalex07/c0f9304deea566842490

## generate key pair
for root (or edit systemd service file to run as other user)
`ssh-keygen -f ~/.ssh/secure-tunnel-<hostname>`

## copy public key to server's authorized_keys
prepend line with `command="",no-pty `
append with key's purpose (`:secure-tunnel` perhaps)

## setup configuration
see `conf.example`
