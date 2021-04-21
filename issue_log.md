
April 2021

first error, after running `bundle install`:
`listen-3.2.1 requires ruby version >= 2.2.7, ~> 2.2, which is incompatible with
the current version, ruby 3.0.1p64`

solution: `bundle update`

next error: 
```
Liquid Exception: tried to create Proc object without a block in _pages/publications.md
jekyll 3.9.0 | Error:  tried to create Proc object without a block
/usr/local/lib/ruby/gems/3.0.0/gems/bibtex-ruby-4.4.7/lib/bibtex/bibliography.rb:150:in `new': tried to create Proc object without a block (ArgumentError)
```

diagnosis: https://github.com/alshedivat/al-folio/issues/161

solution: 

- modify Gemfile as per https://github.com/alshedivat/al-folio/issues/161#issuecomment-751539986
- delete Gemfile.lock
- `bundle update`

