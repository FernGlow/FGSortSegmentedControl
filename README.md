[FGLSortSegmentedControl](http://fernglow.github.com/FGLSortSegmentedControl/Documentation/html/Classes/FGLSortSegmentedControl.html) is a [UISegmentedControl](http://developer.apple.com/library/ios/#DOCUMENTATION/UIKit/Reference/UISegmentedControl_Class/Reference/UISegmentedControl.html) subclass that appends an ascending or descending string to the selected segment's title.

## Screenshots

<img src="https://raw.github.com/FernGlow/FGLSortSegmentedControl/gh-pages/images/FGSortSegmentedControl.gif">

## Getting Started

### 1. Create a sort segmented control

```objective-c
self.segmentedControl = [[FGLSortSegmentedControl alloc] initWithItems:@[@"Name",@"Date",@"Size"]];
self.segmentedControl.segmentedControlStyle = UISegmentedControlStyleBar;
```

### 2. Insert the segmented control into the desired view

```objective-c
self.navigationItem.titleView = self.segmentedControl;
```

The segmented control can be placed in any view.

* As the titleView property of a UINavigationController
* As a UIBarButtonItem in a UIToolbar
* As subview of another view

### 3. Add a target and action to the segmented control for the value changed control event.

```objective-c
[self.segmentedControl addTarget:self action:@selector(updateSortingInformation:) forControlEvents:UIControlEventValueChanged];
```

### 4. Implement the action method specified above

```objective-c	
- (void)updateSortingInformation:(id)sender
{
	NSLog(@"Index %d (%@)", [sender selectedSegmentIndex], [sender isAscending] ? @"Ascending" : @"Descending");
}
```

## Documentation

Read the [full documentation](http://fernglow.github.com/FGLSortSegmentedControl/Documentation/html/index.html)

## Requirements

- iOS 5.1.1
- Apple LLVM 4.0+ (ARC, auto-synthesize, literals and subscripting)

## Contributions

Feel free to fork and submit pull requests. This project is very early in development and I'm open to any improvements.

## License

FGLSortSegmentedControl is available under the MIT license. See the LICENSE file for more info.
