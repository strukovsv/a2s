# a2s

https://github.com/strukovsv/a2s

ascii2svg JavaScript

used compiled program code 
https://github.com/ivanceras/elm-examples/tree/master/elm-bot-lines
by Jovansonlee Cesar
Thank's.

Adapted for used blogger.com and add char asterics "*"

Call a2s from html page

function a2s() {
  $('.a2s').each(function(i, item) {
    var asciitext = $(item).html();
    var source = $(item).attr('source');
    if (source == '1') {
    } else {
        $(item).html("");
    }
    var app = Elm.Main.embed(item);
    app.ports.receiveAsciiText.send(asciitext);
  });
}

$(function() {
    // ascii2svg
    a2s();
});

Example:

<pre class="a2s" source="1">
+------+   +-----+   +-----+   +-----+
|      |   |     |   |     |   |     |
| Foo  +--}| Bar +---+ Baz |{--+ Moo |
|      |   |     |   |     |   |     |
+------+   +-----+   +--+--+   +-----+
              ^         |
              |         V
.-------------+-----------------------.
| Hello here and there and everywhere |
'-------------------------------------'
</pre>
