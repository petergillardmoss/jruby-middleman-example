jruby-middleman-example
=======================

Example of jruby and middleman together.

# Getting started
Please ```. setup``` (assumes Ubuntu)
./make includes example of war and execute

# First commit
`middleman build` runs middleman in jruby succesfully
./make doesn't actually work.  Suffers from the problems outlined in https://github.com/doxavore/warbler144

# Second commit
Introduce bin/main using techniques outlined in https://github.com/doxavore/warbler144 to word around warbler issue
`jruby bin/main` executes succesfully
./make reports the following stack trace:
```
NameError: uninitialized constant Padrino::Helpers::OutputHelpers
  const_missing at org/jruby/RubyModule.java:2684
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-more/core_extensions/default_helpers.rb:17
        require at org/jruby/RubyKernel.java:1082
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core/core_extensions.rb:1
        require at org/jruby/RubyKernel.java:1082
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core/core_extensions.rb:30
        require at org/jruby/RubyKernel.java:1082
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core/application.rb:1
        require at org/jruby/RubyKernel.java:1082
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core/application.rb:18
        require at org/jruby/RubyKernel.java:1082
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core.rb:1
           each at org/jruby/RubyArray.java:1613
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-core-3.1.6/lib/middleman-core.rb:16
           each at org/jruby/RubyArray.java:1613
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-3.1.6/lib/middleman.rb:1
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/middleman-3.1.6/lib/middleman.rb:1
         (root) at jar:file:/home/vagrant/test-war/test-war.jar!/gems/bundler-1.3.5/lib/bundler/runtime.rb:1
        require at jar:file:/home/vagrant/test-war/test-war.jar!/gems/bundler-1.3.5/lib/bundler/runtime.rb:72
           load at org/jruby/RubyKernel.java:1101
        require at jar:file:/home/vagrant/test-war/test-war.jar!/gems/bundler-1.3.5/lib/bundler/runtime.rb:70
        require at org/jruby/RubyKernel.java:1082
        require at jar:file:/home/vagrant/test-war/test-war.jar!/gems/bundler-1.3.5/lib/bundler/runtime.rb:59
        require at jar:file:/home/vagrant/test-war/test-war.jar!/gems/bundler-1.3.5/lib/bundler.rb:132
error: org.jruby.embed.EvalFailedException: (NameError) uninitialized constant Padrino::Helpers::OutputHelpers
``` 


