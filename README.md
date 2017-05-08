# WhenUp

A simple program for importing a Meetup.com group into WhenHub.

> WhenHub lets you transform time-ordered information such as a timeline or schedule into a beautiful, interactive, embeddable Whencast that entertains, educates, and provides chronological context.

It uses the [whenhub gem](https://github.com/mattgillooly/whenhub) to simplify communication with the WhenHub API.

## Usage

You'll need API keys for both [the WhenHub API](https://developer.whenhub.com/),
and [the Meetup.com API](https://www.meetup.com/meetup_api/).

Assign these to the `WHENHUB_TOKEN` and `MEETUP_API_KEY` environment variables, respectively.
(You may save these in a `.env` file to take advantage of the [dotenv gem](https://github.com/bkeepers/dotenv) if you wish.)

You can then invoke the program for a specific meetup group as:

```
$ bundle exec bin/whenup MEETUP_GROUP_URLNAME
```

where `MEETUP_GROUP_URLNAME` is the unique identifier of a Meetup.com group, as seen in the group's URL.

This will then create a new Schedule in your WhenHub account for the Meetup group, with an event for each of that group's events.

### OUTPUT:

```
Created Schedule: 12341234123412341234 with 2 events.
https://studio.whenhub.com/studio#/apps/schedules/12341234123412341234/events
```
