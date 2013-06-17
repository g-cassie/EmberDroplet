Ember Droplet
=============

Ember Droplet allows HTML5 drag and drop functionality in Ember straight out-of-the-box. Its philosophy is that it doesn't
impose anything, and instead allows each individual developer to decide how it should work. I've provided a view &ndash; `EmberDropletView`
that you're free to use in your views. However, most of the functionality exists in the controller mixin &dash; `EmberDropletController`).

For the time being, please refer to the example.

Features
-------------

 * Upload with HTML5's drag and drop;
 * MIME type restrictions on permitted file types;
 * Instant image previews upon dropping;
 * Specifies extension in class name to allow for icons for different file types;
 * Allows the deletion of files before they're uploaded;
 * Keeps a track of all files &ndash; even invalid files;

Methods
-------------

The `EmberDropletController` exposes the following public methods:

 * `addValidFile` &ndash; Adds a file that is allowed by its MIME type;
 * `addInvalidFile` &ndash; Same as above, but a file that isn't allowed by its MIME type;
 * `deleteFile` &ndash; Deletes a specified file by its object;
 * `clearAllFiles` &ndash; Clears all files, including uploaded files;
 * `uploadAllFiles` &ndash; Uploads all valid files;

In addition to the methods, `EmberDropletController` also has the following computed properties for convenience:

 * `validFiles` &ndash; Provides a list of valid files;
 * `invalidFiles` &ndash; Provides a list of invalid files;
 * `uploadedFiles` &ndash; All uploaded files;
 * `deletedFiles` &ndash; All deleted files;

Additional computed properties can be added to your controller that implements the mixin. To add additional computed properties,
please refer to the protected `_filesByProperties` method in the mixin.

Example
-------------

The example uses the Node.js server to upload files, which is available in `example/node-server`. Simply run: `node server` to create it.