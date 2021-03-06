
## <a name="resource-book">Book</a>


A notebook data

### Attributes

| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **_id** | *string* | The unique notebook ID which should start with `book:` and the remains are randomly generated string<br/> **pattern:** `^book:`<br/> **Length:** `6..128` | `"book:9dc6a7a7"` |
| **_rev** | *string* | This is a CouchDB specific field. The current MVCC-token/revision of this document (mandatory and immutable) | `"14-813af5085bb6a2648c3f0aca37fc821f"` |
| **count** | *number* | It indicates the number of notes in the notebook | `42.0` |
| **createdAt** | *number* | The date time when the notebook was created, represented with Unix timestamps in milliseconds | `42.0` |
| **name** | *string* | The notebook name<br/> **Length:** `1..∞` | `"example"` |
| **parentBookId** | *nullable string* | The ID of the parent notebook | `null` |
| **updatedAt** | *number* | The date time when the notebook was last updated, represented with Unix timestamps in milliseconds | `42.0` |


## <a name="resource-file">File</a>


An attachment file

### Attributes

| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **_attachments:index:content_type** | *string* | The content type of the file<br/> **one of:**`"image/png"` or `"image/jpeg"` or `"image/jpg"` or `"image/svg"` or `"image/gif"` | `"image/png"` |
| **_attachments:index:data** | *string* | The file data | `"example"` |
| **_id** | *string* | The unique document ID which should start with `file:` and the remains are randomly generated string<br/> **pattern:** `^file:`<br/> **Length:** `6..128` | `"file:By8_nQtce"` |
| **_rev** | *string* | This is a CouchDB specific field. The current MVCC-token/revision of this document (mandatory and immutable). | `"14-813af5085bb6a2648c3f0aca37fc821f"` |
| **contentLength** | *number* | The content length of the file | `42.0` |
| **contentType** | *string* | The MIME type of the content<br/> **one of:**`"image/png"` or `"image/jpeg"` or `"image/jpg"` or `"image/svg"` or `"image/gif"` | `"image/png"` |
| **createdAt** | *number* | The date time when the note was created, represented with Unix timestamps in milliseconds | `42.0` |
| **name** | *string* | The file name<br/> **Length:** `1..128` | `"example"` |
| **publicIn** | *array* | An array of the note IDs where the file is included | `[null]` |


## <a name="resource-note">Note</a>


A note data

### Attributes

| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **_id** | *string* | The unique document ID which should start with `note:` and the remains are randomly generated string<br/> **pattern:** `^note:`<br/> **Length:** `6..128` | `"note:Bkl_9Vubx"` |
| **_rev** | *string* | This is a CouchDB specific field. The current MVCC-token/revision of this document (mandatory and immutable). | `"14-813af5085bb6a2648c3f0aca37fc821f"` |
| **body** | *string* | The content of the note represented with Markdown<br/> **Length:** `0..1048576` | `"example"` |
| **bookId** | *string* | The notebook ID<br/> **pattern:** `^book:`<br/> **Length:** `6..128` | `"example"` |
| **createdAt** | *number* | The date time when the note was created, represented with Unix timestamps in milliseconds | `42.0` |
| **doctype** | *string* | The format type of the body field. It currently can take markdown only, reserved for the future<br/> **one of:**`"markdown"` | `"markdown"` |
| **migratedBy** | *string* | The type of the data migration | `"migrateAddingParentBookId"` |
| **share** | *string* | The sharing mode of the note<br/> **one of:**`"private"` or `"public"` | `"private"` |
| **status** | *string* | The status of the note<br/> **one of:**`"none"` or `"active"` or `"onHold"` or `"completed"` or `"dropped"` | `"none"` |
| **tags** | *array* | The list of tag IDs | `["tag:a28ca207"]` |
| **title** | *string* | The note title<br/> **Length:** `0..128` | `"example"` |
| **updatedAt** | *number* | The date time when the note was last updated, represented with Unix timestamps in milliseconds | `42.0` |


## <a name="resource-tag">Tag</a>


A note tag

### Attributes

| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **_id** | *string* | The unique tag ID which should start with `tag:` and the remains are randomly generated string<br/> **pattern:** `^tag:`<br/> **Length:** `6..128` | `"tag:0ebd717b"` |
| **_rev** | *string* | This is a CouchDB specific field. The current MVCC-token/revision of this document (mandatory and immutable) | `"14-813af5085bb6a2648c3f0aca37fc821f"` |
| **color** | *string* | The color type of the tag<br/> **one of:**`"default"` or `"red"` or `"orange"` or `"yellow"` or `"olive"` or `"green"` or `"teal"` or `"blue"` or `"violet"` or `"purple"` or `"pink"` or `"brown"` or `"grey"` or `"black"` | `"default"` |
| **count** | *number* | It indicates the number of notes with the tag | `42.0` |
| **createdAt** | *number* | The date time when the tag was created, represented with Unix timestamps in milliseconds | `42.0` |
| **name** | *string* | The name of the tag<br/> **Length:** `0..64` | `"example"` |
| **updatedAt** | *number* | The date time when the tag was last updated, represented with Unix timestamps in milliseconds | `42.0` |


