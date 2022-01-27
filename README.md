# Description

This is a fork of itext 2.1.7 with enhancements for j5.


# Building

To build `lib/iText.jar` run

```
cd src
ant jar
```

# Releasing

Run (Note: the duplicate `v2.1.7.version` is not a typo)

```
git tag -m v2.1.7.<version> v2.1.7.<version>
git push --tags
```

In your ivy repo in `com.j5int/com.lowagie.itext/2.1.7.<version>` create a file
called `ivy-2.1.7.<version>.xml` with content

```
<ivy-module version="2.0">
  <info organisation="com.j5int" module="com.lowagie.text" revision="2.1.7.<version>" publication="<date>"/>
  <publications>
    <artifact name="com.lowagie.text" type="jar" ext="jar"/>
  </publications>
  <dependencies/>
</ivy-module>
```

where `<date>` looks something like `20210127010000`. Copy `lib/iText.jar` into
the same folder and rename it to `com.lowagie.itext-2.1.7.<version>.jar`.

You should also create a GitHub release and upload `ivy-2.1.7.<version>.xml`
and `com.lowagie.itext-2.1.7.<version>.jar` as artifacts.

# License

 Copyright 1999, 2000, 2001, 2002 Bruno Lowagie

 The contents of this file are subject to the Mozilla Public License Version 1.1
 (the "License"); you may not use this file except in compliance with the License.
 You may obtain a copy of the License at http://www.mozilla.org/MPL/

 Software distributed under the License is distributed on an "AS IS" basis,
 WITHOUT WARRANTY OF ANY KIND, either express or implied. See the License
 for the specific language governing rights and limitations under the License.

 The Original Code is 'iText, a free JAVA-PDF library'.

 The Initial Developer of the Original Code is Bruno Lowagie. Portions created by
 the Initial Developer are Copyright (C) 1999, 2000, 2001, 2002 by Bruno Lowagie.
 All Rights Reserved.
 Co-Developer of the code is Paulo Soares. Portions created by the Co-Developer
 are Copyright (C) 2000, 2001, 2002 by Paulo Soares. All Rights Reserved.

 **Contributor(s): Hexagon AB and/or its subsidiaries and affiliates**

 Alternatively, the contents of this file may be used under the terms of the
 LGPL license (the "GNU LIBRARY GENERAL PUBLIC LICENSE"), in which case the
 provisions of LGPL are applicable instead of those above.  If you wish to
 allow use of your version of this file only under the terms of the LGPL
 License and not to allow others to use your version of this file under
 the MPL, indicate your decision by deleting the provisions above and
 replace them with the notice and other provisions required by the LGPL.
 If you do not delete the provisions above, a recipient may use your version
 of this file under either the MPL or the GNU LIBRARY GENERAL PUBLIC LICENSE.

 This library is free software; you can redistribute it and/or modify it
 under the terms of the MPL as stated above or under the terms of the GNU
 Library General Public License as published by the Free Software Foundation;
 either version 2 of the License, or any later version.

 This library is distributed in the hope that it will be useful, but WITHOUT
 ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
 FOR A PARTICULAR PURPOSE. See the GNU Library general Public License for more
 details
