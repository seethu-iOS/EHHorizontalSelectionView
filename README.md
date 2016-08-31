# EHHorizontalSelectionView

This is extension for presenting horisontal lists of items (horisontal tableview)

<img src="https://josshad.github.io/EHHorizontalSelectionView/EHSelView.gif">

## Installation
### Manual
Add files from EHHorizontalSelectionView  to your project 

##Usage
	#import <EHHorizontalSelectionView/EHHorizontalSelectionView.h>

Default style of table is with EHHorizontalViewCell cells. To change default behaviour you need register another cell class or cell nib. Custom cell must subclassed from EHHorizontalViewCell.

For example cell types with animated selection:

	[_hSelView registerCellWithClass:[EHHorizontalLineViewCell class]];
	[_hSelView1 registerCellWithClass:[EHRoundedHorizontalViewCell class]];
	
or your custom cell:

	[_hSelView2 registerCellNib:[UINib nibWithNibName:@"MyCustomCellNib" bundle:nil] withClass:[EHHorizontalViewCell class]];

##Customization

###Color
You can change default tint color for cell of selected type

    [EHHorizontalLineViewCell updateTintColor:[UIColor colorWithHex:0x00c264]];
  
Or you can subclass cell of that type and override method **+ (UIColor * _Nonnull)tintColor;**

    + (UIColor *)tintColor
    {
      return [UIColor redColor];
    }

###Fonts
  
    [EHRoundedHorizontalViewCell updateFontMedium:[UIFont boldSystemFontOfSize:15]];
    [EHRoundedHorizontalViewCell updateFontMedium:[UIFont systemFontOfSize:15]];
    
###Gap wifth between cells

    [EHHorizontalLineViewCell updateCellGap:20];
    
###Line height (for EHHorizontalLineViewCell)

    [EHHorizontalLineViewCell updateColorHeight:2];

##Author
Danila Gusev

<a href="mailto:jos.shad@gmail.com">jos.shad@gmail.com</a>

## License

Usage is provided under the <a href="http://opensource.org/licenses/MIT" target="_blank">MIT</a> License. See <a href="https://github.com/josshad/EHPlainAlert/blob/master/LICENSE">LICENSE</a> for full details.
