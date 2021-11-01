### 1. Put some "includes"
Put some sections of pages that will be used all around. Navbars, head, etc, in their own file.

### 2. Structure these parts with a layout
Create a ceraint structure with the "includes" on the layout page. The layout consists of two main parts: The "includes", and the yield content.

To "copy paste" stuff from the includes into the layout, use `@include('module.path')`

To set a place as a content area, use `@yield('content_name')`

To insert content inside that yield form another file, insert a `@extends('module.path')`, then create a section with `@section('content_name')` with the exact same name as the yield, then close it with `@stop`


You can conditionally render html with the 
`@if(expr)`
`@endif`
also
`@empty($variable)`
`@endempty`

`@unless (empty($name))`
`@endunless`

`@isset()`
`@endisset`

`@for(...)`
`@endfor`

`@foreach($variable as $item)`
`@endforeach`

