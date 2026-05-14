# FORM-EDITOR

Bootstrap Form Builder is a drag-and-drop form editor with three panels: a component palette, a live form canvas, and a properties editor.
Left Panel — Component Palette: Contains 11 draggable input types: Checkbox, Switch, RadioGroup, Select, TextInput, URLInput, Password, Email, TextArea, DatePicker, and a SubmitButton. Each element has an auto-incrementing serial number (e.g. TextInput1, TextInput2...) so every dropped copy gets a unique name.
Middle Panel — Form Canvas: The drop target. Dragging an element from the left clones it into the form, assigns it a unique ID, and links all its controls to the form via the form attribute. Only one Submit button is allowed. Clicking any dropped element selects it (blue border) and loads its properties into the right panel.
Right Panel — Properties Editor: Allows live editing of the selected element:

Rename — updates the label text in real time
Background / Font color — styles the input control directly
Width — resizes the enclosing box (as a percentage), synced between slider and number input
Height — resizes the control itself in pixels, similarly synced
Font family — changes the label's typeface
Required / Disabled — toggles HTML validation attributes on the control
Validate — calls reportValidity() to trigger browser-native validation UI
Random / Clear background — sets or removes a random photo from picsum.photos as the form's background image

Form Submission: The form uses method="GET", so submitting reloads the page with field values in the URL. On load, the script reads window.location.search and logs any received key-value pairs to the console.
