<br />

<div align="center">
  <h3 align="center">SCA Command</h3>

  <p align="center">
    Create commands for your NodeJS Project
    <br />
    <br />
    <a href="https://github.com/mwaqar666/sca-command/issues">Report Bug</a>
    ·
    <a href="https://github.com/mwaqar666/sca-command/issues">Request Feature</a>
  </p>
</div>

## Note

The documentation is under development. You are welcome to review the source code and document it. It will be completed soon. You can explore the code for un-documented features.

## Installation

```shell
npm i sca-command --save
```

## Usage

Register commander as follows

```ts
import { Comander } from "sca-command";

const commandManager = await Commander.start();
```

To create a command

```ts
export class AwesomeCommand extends BaseCommand<TData> {
	public commandName(): string {
		return "awesome-command";
	}

	public async commandAction(commandArguments: KeyValueArgument[], flags: string[]): Promise<void> {
		console.log("This is an awesome command"); // This is an awesome command

		console.log("Command arguments: ", commandArguments);

		console.log("Command flags: ", flags);
	}
}
```

To register command:

```ts
commandManager.registerCommands([
	import("@/somewhere/in/app/awesome.command"),
])
```

Register entry point for commands in `package.json`:

```json lines
{
  //
  "scripts": {
    "my-app": "node dist/index.js awesome-command"
  }
}
```

To run the command manager:

```ts
await commandManager.run();
```

Compile the project and run the below code from command line:

```shell
npm run my-app awesome-command
```

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

## Contact

Yahoo: [mwaqar666@yahoo.com](mailto:mwaqar666@yahoo.com)
<br>
Google: [muhammadwaqar666@gmail.com](mailto:muhammadwaqar666@gmail.com)