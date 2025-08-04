# CommitMono Customized Nerd Font

This repo distributes a customized version of [Commit Mono](https://commitmono.com/) 
that has cv02 and cv11 set to ALT, and patched by [font-patcher](https://github.com/ryanoasis/nerd-fonts?tab=readme-ov-file#font-patcher)
of Nerd Font.

An example usage of the font in conjunction with Nix [home-manager](https://github.com/nix-community/home-manager) can
be found [here](https://github.com/BirkhoffLee/dotfiles/blob/05823e24a46b9405686e412074fd7c2de28c2412/hosts/AlexMBP/home/packages/commitmono-nerd-font.nix).

## custom-settings.json

These settings can be used in Section 07 Customize on [the official website](https://commitmono.com/) to download the unpatched font.

```json
{
	"weight": 400,
	"italic": false,
	"alternates": {
		"cv01": false,
		"cv02": true,
		"cv03": false,
		"cv04": false,
		"cv05": false,
		"cv06": false,
		"cv07": false,
		"cv08": false,
		"cv09": false,
		"cv10": false,
		"cv11": true
	},
	"features": {
		"ss01": false,
		"ss02": false,
		"ss03": true,
		"ss04": true,
		"ss05": true
	},
	"letterSpacing": 0,
	"lineHeight": 1,
	"fontName": ""
}
```

## Nerd Font patching

The official docker image was used to patch the font.

```
docker run --rm -v ./input:/in:Z -v ./out:/out:Z nerdfonts/patcher
```

## License

[Commit Mono](https://commitmono.com/) is released under [SIL Open Font License 1.1](https://openfontlicense.org/documents/OFL.txt).
This is an modified version of the original project.
 
