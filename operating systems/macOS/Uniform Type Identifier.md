---
tags:
  - os
  - macos
---
# Uniform Type Identifier

>All information pulled form [here](https://en.wikipedia.org/wiki/Uniform_Type_Identifier).
>And from [Apple](https://developer.apple.com/library/archive/documentation/FileManagement/Conceptual/understanding_utis/understand_utis_conc/understand_utis_conc.html).

This is essentially a better MIME type as it "eliminates the ambiguities and problems associated with inferring a file's content from its MIME type, filename extension, or type or creator code". Sounds pretty cool.

It has a "reverse-DNS naming structure", meaning that it may include ASCII characters (\[A-Z]\[a-z]\[0-9]\-.) and all Unicode characters above `U+007F`. Mind you that colons and slashes are prohibited for macOS and POSIX file path conventions.

UTI also has a inheritance-like feature wherein certain identifiers conform to certain superclasses:

|Identifier|Conforms to|Comment|
|-|-|-|
|public.item| |base class in the physical hierarchy|
|public.content| |base class for all document content|
|public.data|public.item|base class for all files, byte streams, pasteboard, etc.|
|public.image|public.data, public.content|base class for all images|
|public.text|public.data|base class for all text|
|public.case-insensitive-text|public.text|(unsure) base class for all case-insensitive text|

UTIs are also used to identify other file type identifiers:

|Identifier|Conforms to|Comment|
|-|-|-|
|public.filename-extension|public.case-insensitive-text|filename extension|
|public.mime-type|public.case-insensitive-text|MIME type|
|com.apple.ostype|public.text|four-character code for OSType|
|com.apple.nspboard-type|public.text|NSPasteboard type|

>The documentation of [OSType](https://en.wikipedia.org/wiki/FourCC).

If you need to create a custom or uncommon UTI type, you can create one with a prefix of `dyn.`.

>This naming scheme reminds me of Java packages or some Python imports.
