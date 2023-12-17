# 2 Jan 2023

To generate site:
    bundle exec jekyll serve
- open 127.0.0.1:4000 to preview locally
- site files will be in `_site`

To publish to csxtan.github.io, commit and push all changes EXCEPT Gemfile (the local gemfile is set up for Jekyll, the remote needs to be set up for GitHub Pages workflow).
- should update within 10 minutes, check on Actions tab on GitHub for status.

To publish to math.uchicago.edu/~cindy, connect to UChicago VPN with Cisco and run
    scp _site/* cindy@math.uchicago.edu:~/public_html/
- password is in Bitwarden
- [more info](http://math.uchicago.edu/miscellany/making-a-website/current-website-guide.pdf)
