You can get the application directory where you can, for example, save configuration files with `typer.get_app_dir()`:

```Python hl_lines="9"
{!./src/app_dir/tutorial001.py!}
```

It will give you a directory for storing configurations appropriate for your CLI program for the current user in each operating system.

Check it:

<div class="termy">

```console
$ python main.py

Config file doesn't exist yet
```

</div>

## About `Path`

If you hadn't seen something like that:

```Python
Path(app_dir) / "config.json"
```

A `Path` object can be used with `/` and it will convert it to the separator for the current system (`/` for Unix systems and `\` for Windows).

If the first element is a `Path` object the next ones (after the `/`) can be `str`.

And it will create a new `Path` object from that.

If you want a quick guide on using `Path()` you can check <a href="https://realpython.com/python-pathlib/" target="_blank">this post on Real Python</a> or <a href="https://treyhunner.com/2018/12/why-you-should-be-using-pathlib/" target="_blank">this post by Trey Hunner</a>.