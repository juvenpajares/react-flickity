# Flickity React
Flickity component for React

### Installation
```bash
  npm install flickity --save
  npm install react-flickity --save
```

### Add loaders to webpack config and production files
```js
module: {
    loaders: [
      {
        test: /flickity/,
        loader: 'imports?define=>false&this=>window'
      }
    ]
  }
```

### Download and import flickity to your css

+ CSS:
  - [flickity.css](https://raw.githubusercontent.com/juvenpajares/react-flickity/master/lib/flickity.css)

### Example
```js
var React = require('react')
var Flickity = require('react-flickity')

var flickityOptions = {
    initialIndex: 0,
    cellSelector: '.sliderBoxes',
    accessibility: true,
    pageDots: true,
    wrapAround: true,
    autoPlay: 3000 // default false
}

var Carousel = React.createClass({
    render: function () {
    return (
      <Flickity
        className={ 'carousel' } // default ''
        elementType={ 'div' } // default 'div'
        options={ flickityOptions } // takes flickity options {}
        disableImagesLoaded={ false } // default false
      >
        <div className="sliderBoxes"></div>
        <div className="sliderBoxes"></div>
        <div className="sliderBoxes"></div>
      </Flickity>
    );
  }
});

module.exports = Carousel;
});
```