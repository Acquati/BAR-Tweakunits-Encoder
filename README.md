# BAR Tweakunits Encoder

A tiny client-side web tool that converts a [Beyond All Reason](https://www.beyondallreason.info/) tweakunits table into the encoded `!bset tweakunits` chat command.

## Usage

Open `index.html` in a browser. Paste a BAR tweakunits table into the input panel and the encoded command is generated live:

```
!bset tweakunits <base64>
```

Example input:

```
armaak = {
  unitrestricted = 0,
},
```

## How it works

1. The input text is UTF-8 encoded and converted to standard Base64.
2. Base64 padding characters (`=`) are replaced with `_` so the result is safe to paste into the in-game chat console.
3. The result is prefixed with `!bset tweakunits `.

Everything runs in the browser — no server, no build step, no dependencies beyond [Prettier](https://prettier.io/) for formatting.

## Commands

| Command                | Description                    |
| ---------------------- | ------------------------------ |
| `npm run format`       | Format all files with Prettier |
| `npm run format:check` | Check formatting with Prettier |

## License

[MIT](LICENSE)
