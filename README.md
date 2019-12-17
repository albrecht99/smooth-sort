

# <div align="center">Smooth Sort</div>

<div align="center">  
<a href="https://flutter.io">  
    <img src="https://img.shields.io/badge/Platform-Flutter-yellow.svg"  
      alt="Platform" />  
  </a>  
  <a href="https://opensource.org/licenses/MIT">  
    <img src="https://img.shields.io/badge/License-MIT-red.svg"  
      alt="License: MIT" />  
  </a>  
  </div> 
<div align="center">A wonderful and custom sorting animation for Flutter.</div>
<div align="center">In today's world, developer's use now and then sorting in their mobile applications. For such developer's, Smooth Sort can become a useful package which provides wonderful and custom animation while sorting a list instead of reloading the app.</div>

# Table of Contents
* [Demo](#demo)
* [Usage](#usage)
* [Documentation](#documentation)
* [Algorithm](#algorithm)
* [Bugs or Requests](#bugs-or-requests)
* [License](#license)

# Demo
<div align="center">
<table>
<tr>
<td>
<div align="center">Flip Vertically</div>
<div align="center">animationType: flipVertically</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/flipVertically.gif" height = "400px"/>  
</td>
<td>
<div align="center">Fade</div>
<div align="center">animationType: fade</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/fade.gif" height = "400px"/>  
</td>
<td>
<div align="center">Slide Right</div>
<div align="center">animationType: slideRight</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/slideRight.gif" height = "400px"/>  
</td>
</tr>
<tr>
<td>
<div align="center">Flip Horizontally</div>
<div align="center">animationType: flipHorizontally</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/flipHorizontally.gif" height = "400px"/>  
</td>
<td>
<div align="center">Scale</div>
<div align="center">animationType: scale</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/scale.gif" height = "400px"/>  
</td>
<td>
<div align="center">Slide Left</div>
<div align="center">animationType: slideLeft</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/slideLeft.gif" height = "400px"/>  
</td>
</tr>
<tr align="center">
<td>
<div align="center">Reverse Flip Vertically</div>
<div align="center">animationType: reverseFlipVertically</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/reverseFlipVertically.gif" height = "400px"/>  
</td>
<td>
<div align="center">Reverse Flip Horizontally</div>
<div align="center">animationType: reverseFlipHorizontally</div>
<br>
<img src="https://raw.githubusercontent.com/mdg-soc-19/smooth-sort/master/smoothSortGifs/reverseFlipHorizontally.gif" height = "400px"/>  
</td>
</tr>
</table>
</div>

# Usage
For adding the SmoothSort in your Flutter app, you have to simply provide the options for ListView or GridView with the list of the widgets to be displayed in the list/grid with the another list of their corresponding itemIds.

For example:
First create the object for SmoothSort 
```dart
SmoothSort smoothSort = SmoothSort(
	listType: 'list',	 // specify the listType i.e. list or grid
	itemList: [  
	  Container(  
	    color: Colors.red,  
	    alignment: Alignment.center,  
		child: Text(  
		    "A",  
	        style: TextStyle(fontSize: 150.0),  
		    ),  
	  ),  
	  Container(  
	    color: Colors.blueAccent,  
	    alignment: Alignment.center,  
	    child: Text(  
		    "B",  
	        style: TextStyle(fontSize: 150.0),  
			),  
	  ),  
	  Container(  
	    color: Colors.yellowAccent,  
	    alignment: Alignment.center,  
	    child: Text(  
		    "C",  
	        style: TextStyle(fontSize: 150.0),  
			),  
	  ),   
	],					// specify the list of widgets for the ListView/GridView
	itemIdList: [1, 2, 0],		// specify the corresponding ids for widgets	
	animationType: 'cardScale'	// specify the type of animation you want
);
```

Whenever you want to add the list or grid, just add the above widget as follows:
```dart
Column(  
  children: <Widget>[  
    smoothSort	// just add the SmoothSort object
  ],
),
```

After this, just call the `smoothSort.onPress()` method to start the animation for sorting the list/grid just like this:
```dart
RaisedButton(  
  child: Text("Sort"),  
  onPressed: () {  
    smoothSort.onPress();	// just call the onPress method
  },  
)
```
For more info, please refer to the  `main.dart`  in example.

# Documentation

### SmoothSort Class

| Dart attribute                        | Datatype                    | Description                                                  |     Default Value     |
| :------------------------------------ | :-------------------------- | :----------------------------------------------------------- | :-------------------: |
| listType                                 | String                  | Specifies the type of list i.e. list/grid.               |       list       |
| animationType                             | String             | Specifies the type of animation required to sort the list/grid. |       flipVertically       |
| itemList                                | List&lt;Widget&gt;                      | The list of widgets which is to be sorted. |         @required         |
| itemIdList                           | List&lt;int&gt;                      | This list contains the ids for the corresponding widgets needed for the sorting of widgets. |          @required          |
| gridCrossAxisCount            | int                        | The number of grids in a single row in GridView.             |         2          |

For help on editing package code, view the [flutter documentation](https://flutter.io/developing-packages/).

# Algorithm
The algorithm used to build this project is as follows:

I have sorted the ListView or GridView with single TextView by using the default sort function by Dart language. On clicking of the sort button, I have provided different animations to the ListView or GridView according to the animation described by the user. 

For more info, please refer to the  `smooth_sort.dart`.

# Bugs or Requests  
  
If you encounter any problems feel free to open an issue. If you feel the library is  
missing a feature, please raise a ticket on Github and I'll look into it.  
Pull request are also welcome.  

# License

SmoothSort is licensed under `MIT license`. View [license](https://github.com/mdg-soc-19/smooth-sort/blob/master/LICENSE).
