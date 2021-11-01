### 1. Put some "includes"
Put some sections of pages that will be used all around. Navbars, head, etc, in their own file.

### 2. Structure these parts with a layout
Create a ceraint structure with the "includes" on the layout page. The layout consists of two main parts: The "includes", and the yield content.

To "copy paste" stuff from the includes into the layout, use `@include('module.path')`

To set a place as a content area, use `@yield('content_name'`