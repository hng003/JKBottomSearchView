# JKBottomSearchView
[![Build Status](https://travis-ci.org/JaroVoltix/JKBottomSearchView.svg?branch=master)](https://travis-ci.org/JaroVoltix/JKBottomSearchView)

## Installation

### Cocapods
``` Coming soon```

### Carthage 
``` github "JeyKeyCom/JKBottomSearchView"```

## Requirment
 - iOS 9+
 - Xcode 9+
 - Swift 4.1+
 
## Usage
Create JKBottomSearchView 
```
func viewDidLoad(){
    super.viewDidLoad()
    let searchView = JKBottomSearchView()
    view.addSubview(searchView)
}
```
### DataSource & Delegate
JKBottomSearchViewDataSource is and alias to UITableViewDataSource. 

```
extension ViewController:JKBottomSearchViewDataSource{}
```
```
searchView.dataSource = self
```

JKBottomSearchViewDelegate is an alias for UITableViewDelegate & UISearchBarDelegate.

```
extension ViewController:JKBottomSearchViewDelegate{}
```
```
searchView.delegate = self
```

### Customization
```
//Change blur effect. Default nil
searchView.blurEffect = UIBlurEffect(style: .dark)

//Any non tableView and searchBar customization should be performed on contentView
searchView.contentView.backgroundColor = .red

//Customizing searchBar
searchView.barStyle = .black 
searchView.searchBarStyle = .minimal 
searchView.searchBarTintColor = .black
searchView.placeholder = "What are you looking for"
searchView.showsCancelButton = true
searchView.enablesReturnKeyAutomatically = true

//Customizing searchBar textField
let textField = searchView.searchBarTextField
textField.textColor = .red

```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
