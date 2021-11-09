###  Avatar Layers (top level)

- **Name** *required*
	string
	Name assigned to the layer (mission control only)
	
- **Position** *required*
	int
	Layer order (z-index) of the avatar parts when combined, 
	Must be unique
	
- **CanBeEmpty**
	True/False
	Sets whether an item must be present for the layer

- **GroupId** *required*
	int
	Grouping to display the layer selector in
	Combination of GroupId/SortOrder must be unique

- **SortOrder** *required*
	int
	Order within its group to display the layer selector
	Combination of GroupId/SortOrder must be unique
	
- **DefaultLayer**
	True/False
	Sets the layer to be selected by default when loading the avatar page
	Only one layer can be the default

- **ShowItemSelector**
	True/False
	Sets whether the item selector should be shown for the layer
	Should only be true if the layer contains multiple items
	
- **ShowColorSelector**
	True/False
	Sets whether the color selector should be shown for the layer
	Should only be true if the layer contains multiple colors
	
- **ZoomScale** *required*
	decimal
	Amount to zoom when viewing avatar selector on a mobile device
	Values > 1 zooms in, values < 1 zoom out
	
- **ZoomXOffset**
	int
	Amount to shift the y-asix when viewing avatar selector on a mobile device
	Positive values shift the view down, negative values shift the view up
	
-  **Texts** (*required for each language*)

	- **Language** *required*
		string
		IETF BCP 47 language tag
		
	- **Name** *required*
		string
		Name to be displayed for the layer in the associated language

- **AvatarColors** (*required if layer uses colors*)

	- **Colors** *required*
		string
		Hexcode to display in the color selector

	- **SortOrder** *required*
		int
		Order to display the color for the layer
		Must be unique within the layer

- **AvatarItems** *required*

	- **Name** *required*
		string
		Name assigned to the item (mission control only)

	- **SortOrder** *required*
		int
		Order to display the item for the layer
		Must be unique within the layer
		
	- **Unlockable**
		True/False
		True hides the item from the selector unless it's unlocked for a user through a trigger
