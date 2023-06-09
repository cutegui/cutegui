# Cute GUI
Core repository of CuteGUI project

CuteGUI that framework for desktop applications, written
in Rust programming language.

The main goals of project are:
* Easy to use
* Maximize performance
* Cross-platform
* Native

# Common structure
- my_app
    - assets
      - some_image.png
      - some_font.ttf
      - ...
    - storage
      - storage.rs
    - router
      - router.rs
    - components
      - person_card.cg
      - header.cg
    - screens
      - main_screen.cg
    - app.cg
    - main.rs

simple screen component should look like that:
```html
<template>
    <div>
        <p> {{ text }} </p>
        <p> Hello world! </p>
    </div>
</template>

<css>
    div {
        background-color: #000000;
    }
</css>

<rust>
use cutegui::component::Storage;

let component_storage = Storage::new();
component_storage.set("text", "Hello world!");
</rust>
```

