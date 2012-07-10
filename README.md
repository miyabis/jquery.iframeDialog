jQuery UI Dialog iframe wrapper Plugin
======================

is a wrapper for the dialog to display the external content using an iframe.

Sample Code
----------

``` html
<html>
<head>
	<script type="text/javascript" src="http://code.jquery.com/jquery-1.7.2.min.js"></script>
	<script type="text/javascript" src="http://code.jquery.com/ui/1.8.19/jquery-ui.min.js"></script>
	<script type="text/javascript" src="../jquery.iframeDialog.js"></script>
	<script type="text/javascript">
		$(function(){
			$('#dialogOpen1').iframeDialog({
				modal: true,
				resizable: false,
				width: 200,
				height: 200
			});
			$('#dialogOpen2').iframeDialog({
				/* iframeDialog options */
				id: 'iframeDialogTest',
				url: 'test.html',
				scrolling: 'auto',
				/* jquery UI Dialog options */
				title: 'iframe Dialog',
				modal: true,
				resizable: true,
				width: 200,
				height: 200,
				buttons: {
					'close': function() {
						$(this).remove();
					}
				}
			});
		});
	</script>
	<link href="http://code.jquery.com/ui/1.8.19/themes/base/jquery-ui.css" rel="stylesheet"/>
</head>
<body>
	<a id="dialogOpen1" title="iframe Dialog" href="test.html">Dialog Open 1</a><br/>
	<a id="dialogOpen2" href="#">Dialog Open 2</a>
</body>
</html>
```

Option
----------
+   `id` :
    to set the id to the div tag of the dialog.
    id='xxxxx' -> aria-labelledby="ui-dialog-title-xxxxx"

+   `url` :
    Sets the url of the external page.
    
+   `scrolling` :
    to set the scrolling attribute of iframe.
    The default is "no".

License
----------
Copyright &copy; 2012 MiYABiS
Distributed under the [MIT License][mit].
 
[MIT]: http://www.opensource.org/licenses/mit-license.php

Revision 1.1
----------
+   added `id` option.
