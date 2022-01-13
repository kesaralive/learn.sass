# Setup

### Dev Environment Setup

- Visual Studio Code
- Live Sass Compiler
- Live Server

> **Note:** The **Watch now** button is enabled when you're saving sass files.

# SCSS Syntax

    @mixin button-base()
        @include typography(button)

        display: inline-flex
        position: relative
        height: $button-height
        border: none
        vertical-align: middle

        &:hover
            cursor: pointer

# Variables

### SCSS

    $base-color: #c6538c;
    $border-dark: rgba($base-color, 0.88);

    .alert {
    border: 1px solid $border-dark;
    }

### CSS

    .alert {
    border: 1px solid rgba(198, 83, 140, 0.88);
    }

# Functions

### SCSS

    // Font weight class
    $font-weights:("regular":400,
        "medium":500,
        "bold":700,
    );

    // Font weight function
    @function weight($weight-name) {
        @return map-get($font-weights, $weight-name);
    }

    // Uses
    p {
        font-weight:weight(medium);
    }

### CSS

    p {
        font-weight: 500;
    }
