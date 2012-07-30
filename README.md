# Rebar JS Uglifier Plugin

Minify your JavaScript files when building your Erlang OTP
application using UglifyJS.

## Installation

Specify ```rebar_js_uglifier_plugin``` as a dependency in your ```rebar.config```.

```erlang
{deps, [
       {rebar_js_uglifier_plugin, ".*",
        {git, "git://github.com/cmeiklejohn/rebar_js_uglifier_plugin.git", {branch, "master"}}}
]}.
```

Then, configure as a plugin in your ```rebar.config```.

```erlang
{plugins, [rebar_js_uglifier_plugin]}.
```

## Configuration

Below is an example configuration with one minification.  In this example ```vendor.js``` is the destination minified file, sourced from ```vendor.js```.  Place the below configuration in your applications ```rebar.config```.

```erlang
{js_uglify, [
    {doc_root,   "priv/assets/javascripts"},
    {out_dir,    "priv/www/javascripts"},
    {compressions, [
        {"vendor.min.js", "vendor.js"}
    ]}
]}.
```
