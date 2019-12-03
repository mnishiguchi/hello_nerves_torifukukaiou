# HelloNerves

- Weather.Forecast.run means getting "http://weather.livedoor.com/forecast/webservice/json/v1?city=#{city}".
- HelloNerves.update means ExTwitter.update.
- HelloNerves.Scheduler.start_link/0 causes repeatedly to post Japanese Weather Forecast to Twitter at 22:00 UTC.

## Targets

Nerves applications produce images for hardware targets based on the
`MIX_TARGET` environment variable. If `MIX_TARGET` is unset, `mix` builds an
image that runs on the host (e.g., your laptop). This is useful for executing
logic tests, running utilities, and debugging. Other targets are represented by
a short name like `rpi3` that maps to a Nerves system image for that platform.
All of this logic is in the generated `mix.exs` and may be customized. For more
information about targets see:

https://hexdocs.pm/nerves/targets.html#content

## Getting Started

To start your Nerves app:
  * `export MIX_TARGET=my_target` or prefix every command with
    `MIX_TARGET=my_target`. For example, `MIX_TARGET=rpi3`.
    I use `MIX_TARGET=rpi2`
  * `export NERVES_NETWORK_SSID=ssid`
  * `export NERVES_NETWORK_PSK=secret`
  * `export TWITTER_CONSUMER_KEY=xxx`
  * `export TWITTER_CONSUMER_SECRET=yyy`
  * `export TWITTER_ACCESS_TOKEN=zzz`
  * `export TWITTER_ACCESS_TOKEN_SECRET=aaa`
  * `export TEXT_TO_SPEECH_API_KEY=ttt`
  * Install dependencies with `mix deps.get`
  * Create firmware with `mix firmware`
  * Burn to an SD card with `mix firmware.burn`

## Learn more

  * Official docs: https://hexdocs.pm/nerves/getting-started.html
  * Official website: https://nerves-project.org/
  * Forum: https://elixirforum.com/c/nerves-forum
  * Discussion Slack elixir-lang #nerves ([Invite](https://elixir-slackin.herokuapp.com/))
  * Source: https://github.com/nerves-project/nerves
