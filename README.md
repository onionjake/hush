# Human Shell (hush)

The Human Shell is a shell that interprets natural language.  Here is an
example hush script:

```hush
#!/usr/bin/env hush

create the file blah.txt
write hello there to the file blah.txt
rename the file blah.txt to hello.txt
display the contents of hello.txt
delete hello.txt
```

## Use 

```bash
# interactive
./hush
# run a script
./hush <HUSH_SCRIPT>
# Use she-bang in script (see above): #!/path/to/hush
chmod +x <HUSH_SCRIPT>
./<HUSH_SCRIPT>
```

## What can `hush` do?

Currently `hush` understands the following intended actions:

* Create file
* Delete file
* Display file
* Rename file
* Write file
* Exit shell
* ...
* `TODO`

## Installation

`hush` requires the following: 

* ruby
* wit rubygem

The wit rubygem also has pre-requisites, see here: https://wit.ai/docs/ruby/1.0.5

For example, on ubuntu:
```bash
sudo apt-get install libsox-dev libcurl4-openssl-dev ruby-dev build-essential libssl-dev
sudo gem install bundler

cd <path_to_hush>/
bundle install
```

## FAQ
### How does it work?

`hush` uses https://wit.ai/ to do natural language processing.  Wit.ai returns
the command's intended action and what entities it should operate on that.
`hush` then creates a real shell command and executes it.

### Can I add my own commands?

Yes, you can fork my wit.ai instance and train your own commands.  This is my
instance:

https://wit.ai/onionjake/hush

Pull requests are also welcome!

### Does `hush` only speak English?

Yes.  However, wit.ai supports multiple languages, so it should be
straightforward to more to `hush`.


## License

```
   Copyright 2015 Jacob Willoughby

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
