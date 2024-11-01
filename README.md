# Math

Repository for math related work

## Development

### Dependencies

1. [Jekyll](https://jekyllrb.com/docs/)
1. [Bundler](https://bundler.io/)

### Workflow

Every chain of shell commands shall start from the repository root

#### GitHub Pages local preview run

1. ```bash
	cd gh-pages
	```

1. Install Ruby Gems:
	```bash
	bundle install
	```

1. Run Jekyll site locally
	```bash
	bundle exec jekyll serve --watch --livereload livereload_min_delay 10 open_url true
	```

#### Git

1. Create `gh-pages` targeted git subtree and push to remote branch (first time):
	```bash
	git subtree push --prefix gh-pages origin gh-pages
	```
