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

## Installation 

### Pre-reqs

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

### License

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
