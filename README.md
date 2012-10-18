# Fluent::Plugin::Modbus

Fluent plugin to retrieve data from Modbus device 

## Installation

Add this line to your application's Gemfile:

    gem 'fluent-plugin-modbus'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fluent-plugin-modbus

## Usage

    # modbus.conf
    <source>
      type modbus
      tag modbus.server1
      hostname 192.168.0.1
      port 12345 
      polling_time 0,10,20,30,40,50
    </source>

    <match modbus.b>
      type file
      path /var/log/modbus
    </match>

## TODO

* Complete TestCase
* Detailed Register address configuration

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request