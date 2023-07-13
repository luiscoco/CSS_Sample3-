# CSS_Sample4-scss

Open the application folder in VSCode.

To run the application just run the command:
```
npm run start
```

Navigate to the URL: http://localhost:1234

## index.html

```html
<!DOCTYPE html>
<html>
	<head>
		<title>SCSS playground</title>
		<meta charset="UTF-8" />
		<link rel="stylesheet" href="./src/styles/main.scss"></style>
		<script src="./src/scripts/index.ts"></script>
	</head>

	<body>
		<div id="app"></div>
		     <div class="parent">
                          <div class="child">
		          </div>
		     </div>
	  </br>
		<div class="parent--round">
			<div class="child--round"></div>
		</div>
	</body>
</html>
```


## main.scss

```scss
@use "_variables" as *;
@use "_mixins" as *;
@use "_placeholders" as *;

.parent {
  background-color: $parent-bgColor;
  @include size(100px, 150px);
  @include center(center);
  @extend %border;

  &--round {
    background-color: $parent-bgColor;
    @include size(100px);
    @include center(end, end)
  }
}

.child {
  background-color: $child-bgColor;
  @include size(50px, 25px);
  @extend %border;
  @include scaleOnHover;

  &--round {
    background-color: $child-bgColor;
    @include size(50px);
    @include scaleOnHover;
  }
}
```

## package.json

Pay attention to the dependencies, we use "sass" preprocessor.

```json
{
  "name": "js-academy-pw-15",
  "version": "1.0.0",
  "description": "",
  "main": "index.html",
  "scripts": {
    "start": "parcel index.html --open",
    "build": "parcel build index.html"
  },
  "dependencies": {
    "parcel-bundler": "^1.6.1"
  },
  "devDependencies": {
    "@babel/core": "7.2.0",
    "sass": "^1.63.6",
    "typescript": "^5.1.6"
  },
  "resolutions": {
    "@babel/preset-env": "7.13.8"
  },
  "keywords": []
}
```
