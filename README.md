# acmeelixir

Slighly changed version of [acmego](https://github.com/9fans/go/blob/main/acme/acmego/main.go) for Elixir.

`Acmego` assumes that a code formatter takes a filename and prints the body of the formatted code.
`mix format` prints formatted code on `stdout` if input is send as `stdin`, but formats code in place if a filename is provided.

`Acmeelixir` patches `acmego` accordingly and listens for changes of `.ex` and `.exs` files.
If a `.ex` or `.exs` file is written, `acmeelixir` checks whether the file needs changes by running `mix format -`.
If so, it makes the changes in the window body but does not write the file.

