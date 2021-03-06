# Covid19 GraphQL API

https://covid19-graphql.now.sh

[![Deploy with ZEIT Now](https://zeit.co/button)](https://zeit.co/import/project?template=https://github.com/rlindskog/covid19-graphql)


Data is pulled directly from https://github.com/pomber/covid19, which is a JSON representation of https://github.com/CSSEGISandData/COVID-19. All data is up to date.

Example query
```graphql

query {
  # time series data
  results (countries: ["US", "Canada"], date: { lt: "3/10/2020" }) {
    country {
      name
    }
    date
    confirmed
    deaths
    recovered
    growthRate
  }

  # by country
  country(name: "US") {
    name
    mostRecent {
      date(format: "yyyy-MM-dd")
      confirmed
    }
  }
}

```

Zeit verified open source: https://covid19-graphql.now.sh/_src

## Projects using this API

- [I am Covid -19 🦠](https://iamcovid-19.netlify.com/) ([repo](https://github.com/cryptodoct0r/Covid-19-Status-gql)) - Visualization of the covid-19 dataset using Nuxtjs(vuejs), Graphql and valuable information about geeting through the Covid-19 pandemic.

[Add yours +](https://github.com/rlindskog/covid19-graphql/edit/master/README.md)

## License
MIT Licensed. PRs welcome! :)
