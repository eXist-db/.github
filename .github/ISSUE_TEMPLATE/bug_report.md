---
name: Bug report
about: Create a report to help us improve
title: "[BUG]"
labels: ''
assignees: ''

---

> To be able to better understand you problem, please add as much information as possible to this ticket. Always test your bugs against the latest stable release of exist. We cannot provide support for older versions here on GitHub. If the version of eXist that is experiencing the issue is more than 1 major version behind the most recent release, please consider posting a question on our mailing list. 


**Describe the bug**
A clear and concise description of what the bug is.

**Expected behavior**
A clear and concise description of what you expected to happen.

**To Reproduce**
> The *best* way is to provide an [SSCCE (Short, Self Contained, Correct (Compilable), Example)](http://sscce.org/). One type of SSCCE could be a small test which reproduces the issue and can be run without dependencies. Please locate the existing test-suite and follow the examples provided there:

**Unit Test**
Xquery code is tested via [XQSuite - Annotation-based Test Framework for XQuery](http://exist-db.org/exist/apps/doc/xqsuite.xml) test. 
```Xquery
xquery version "3.1";

module namespace t="http://exist-db.org/xquery/test";
declare namespace test="http://exist-db.org/xquery/xqsuite";

<-- Adjust to your reported issue -->
declare
    %test:assertTrue
function t:test() {
    1 eq 1
};
```

Javascript code uses [mocha](https://mochajs.org) 

```javascript
const assert = require('assert')

// this is a dummy test 
describe('Array', function () {
  describe('#indexOf()', function () {
    it('should return -1 when the value is not present', function () {
      assert.strictEqual([1, 2, 3].indexOf(4), -1)
    })
  })
})
```

**Integration Test**
For UI and browser based testing we use [cypress.js](https://www.cypress.io)

```javascript
// adjust as necessary
describe('The app', function() {
  it('should load', function() {
    // Go to app start page
    cy.visit('/app/index.html')
  })
```

If none of the above is working, please tell us the exact steps you took when you encountered the problem:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Context (please always complete the following information):**
 - OS: [e.g. macOS 10.14.6]
 - eXist-db Version: [e.g. 5.1.1]
 - Java Version: [e.g. Java8u121]
-  App Version: [e.g. 1.0.0]

**Additional context**
- How is eXist-db installed? [e.g. JAR installer, DMG, … ]
- Any custom changes in e.g. `conf.xml`?
