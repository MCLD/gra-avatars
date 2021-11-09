# default avatars.json

The `default avatars.json` file describes the configuration of avatar layers and how [The Great Reading Adventure](https://github.com/MCLD/greatreadingadventure) software imports the files present in the ZIP file containing avatar image elements.

The JSON file contains an `array` of Avatar Layer objects.

## Avatar Layer

- **Name** - _required_ - `string` - Name assigned to the layer (for management in Mission Control, not visible to participants)

- **Position** - _required_ - `int` - Layer order (z-index) of the avatar parts when combined, must be unique per layer

- **CanBeEmpty** - `True` or `False` - Sets whether an item must be present for the layer

- **GroupId** - _required_ - `int` - Grouping to display the layer selector in, combination of GroupId/SortOrder must be unique

- **SortOrder** - _required_ - `int` - Order within its group to display the layer selector, combination of GroupId/SortOrder must be unique

- **DefaultLayer** - `True` or `False` - Sets the layer to be selected by default when loading the avatar page, only one layer can be the default

- **ShowItemSelector** - `True` or `False` - Sets whether the item selector should be shown for the layer, only true if the layer contains multiple items

- **ShowColorSelector** - `True` or `False` - Sets whether the color selector should be shown for the layer, only true if the layer contains multiple colors

- **ZoomScale** - _required_ - `decimal` - Amount to zoom when viewing avatar selector on a mobile device: values > 1 zooms in, values < 1 zoom out

- **ZoomXOffset** - `int` - Amount to shift the y-asix when viewing avatar selector on a mobile device: positive values shift the view down, negative values shift the view up

- **Texts** - _required for each language_ - `array`

  - **Language** - _required_ - `string` - IETF BCP 47 language tag

  - **Name** - _required_ - `string` - Name to be displayed for the layer in the associated language

- **AvatarColors** - _required if layer uses colors_ - `array`

  - **Colors** - _required_ - `string` - Hexcode to display in the color selector

  - **SortOrder** _required_ - `int` - Order to display the color for the layer, must be unique within the layer

- **AvatarItems** - _required_ - `array`

  - **Name** - _required_ - `string` - Name assigned to the item (for management in Mission Control, not visible to participants)

  - **SortOrder** - _required_ - `int` - Order to display the item for the layer - must be unique within the layer

  - **Unlockable** - `True` or `False` - True hides the item from the selector unless it's unlocked for a user through a trigger
