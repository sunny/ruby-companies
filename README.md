# Ruby Companies

![GitHub Workflow Status (with branch)](https://img.shields.io/github/actions/workflow/status/calvinwalzel/ruby-companies/gh-pages.yml?branch=main)

[ruby-companies.org](https://ruby-companies.org) is a simple list of companies developing software with Ruby, published collaboratively with the Ruby community. This project is heavily inspired by [RubyConferences.org](https://rubyconferences.org/).

## Eligible Companies

For now, any company that works with Ruby (or a framework based on Ruby). Especially contributions of smaller companies are welcome!

## Contributing

The list of companies is driven by the `src/_companies` directory.

### Adding a company
If you want to add a company, create a file with the following structure: `src/_companies/{continent}/{country}/{region}/{company}/index.md`. Then add at least the required YAML keys (see below) and send a PR.

### Updating a company
If you want to update a company, identify the YAML file and update the outdated or missing information and send a PR.

### List of keys
Here is a list of the keys that can be used:

#### Required
- `name`: The name of the company.
- `continent`: The continent of the company headquarter.
- `country`: The country the company headquarter is based in.
- `region`: The region the company headquarter is based in.
- `city`: The city the company headquarter is based in.
- `website`: The url of the company website.
- `created_at`: The timestamp when the company was created. We use this to determine the newest companies. The easiest way to generate is: `bin/bridgetown company:timestamp`. This will generate a UTC timestamp of the current moment.

#### Optional
- `careers_page`: A url of the careers page for the company.
- `work_arrangements`: An array of the work arrangements the company offers. Possible values: `remote`, `hybrid`, `onsite`.
- `stack`: An array that describes (part of) the stack that the company uses. The first three values are also shown on the overview list, so it's important to hire the key tech here (usually language/framework, database, frontend framework). For a list of already added stacks see `src/_data/stacks.yml`. Feel free to add new values in that file. The klasses value contains [TailwindCSS](https://tailwindcss.com) classes. The text class color should be based on the brand color. [This tool](https://find-nearest-tailwind-colour.netlify.app/) can be used to find the closest Tailwind color from the palette. The background color should be the same color, but the `-100` shade of it. You can deviate from this if it doesn't look good.

## Getting started

The website is built with [Bridgetown.rb](https://www.bridgetownrb.com/).

Install Ruby, then:

```bash
cd ruby-companies
bundle install && yarn install
bin/bridgetown start
```

and point your browser at [http://localhost:4000/](http://localhost:4000/)

In case you want to submit a contribution:
1. Fork the repository
2. Clone the fork using `git clone` to your local development machine.
3. Create your contribution branch (`git checkout -b my-contribution
4. Commit your changes (`git commit -am 'Add ACME company'`)
5. Push to the branch (`git push origin my-contribution
6. Create a new Pull Request

## License

I'm not sure what the best license for this would be, but I'm open to suggestions.
