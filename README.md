# Invalid Imports Example

* Run `npm install`
* Run `bazel build :ng_libs`
* Run `bazel build //src`
* Open `bazel-bin/src/app.component.ngfactory.js` and you will see this import `import * as i0 from "@angular/core";` It is correct.
* Open `bazel-bin/src/app.module.ngfactory.js` and you will see this:

```
import * as i0 from "@angular/core";
import * as i1 from "./app.module";
import * as i2 from "./app.component";
import * as i3 from "./app.component.ngfactory";
import * as i4 from "@angular/core/core";
import * as i5 from "@angular/common/common";
import * as i6 from "@angular/platform-browser/platform-browser";
```

"@angular/core/core", "@angular/common/common", and "@angular/platform-browser/platform-browser" are incorrect. They should be "@angular/core". Running NGC creates factory files with correct imports