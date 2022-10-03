# FlutterLayouts
## Exercice 1     
<img src="https://github.com/mouniraz/FlutterLayouts/blob/main/layouts1.JPG"/>  
<p>purpose of this activity is to do this Layut using the widgets Row et Col </p> 
<h2>Structure of widget1</h2>
1. create a MaterialApp with a Scaffold 

```dart
MaterialApp(
      title: title,
      home: Scaffold(
        appBar: AppBar(
          title: Text(title),
        ),
        body:Text("Widgets Flutter")
        ))
```
3.  create a widget Column having 3 Rows as children, the size of column will be the content size
```dart
Column(mainAxisSize: MainAxisSize.min,
        children: [Row(children: [Text("row1")],),
        Row(children: [Text("row2")],),
        Row(children: [Text("row3")],)])
```
3. the first Row will contain an icon (flutter_dash, color:light:Blue) with Text
```dart
Row(children: [Icon(Icons.flutter_dash,color: Colors.lightBlue),Text("row1")],)
```
5. the second Row contain Text 
```dart
Text("Flutter est un kit de développement logiciel d´interface utilisateur open-source créé par GoogleIl est utilisé pour développer des applications pour Android, iOS, Linux, Mac, Windows, Google Fuchsia et le web à partir d´une seule base de code.")
```
7. The Third Row contain a Text and Icon (arrow_forward, color:light:Blue)
```dart
  Row(children: [Text("EXPLORE_FLUTTER"),Icon(Icons.arrow_forward,color:Colors.lightBlue)],)
```
## Shaping of widgets
in this step we will add some shaping to widgets
1. Add padding right 8dp to first icon 
```dart
Padding(padding: EdgeInsets.only(right: 8),
          child:Icon(Icons.flutter_dash,color: Colors.lightBlue)),
```
2. Add a vertical and horizontal padding to Text of second Row
```dart
Padding(
              padding: EdgeInsets.symmetric(
                vertical: 16.0,
                horizontal: 0,
              ),
              child: Text("Flutter est un kit de développement logiciel d´interface utilisateur open-source créé par GoogleIl est utilisé pour développer des applications pour Android, iOS, Linux, Mac, Windows, Google Fuchsia et le web à partir d´une seule base de code."))
              
```
3. Add a left padding to icon of third Row
```dart
Padding(padding: EdgeInsets.only(left:8),child:Icon(Icons.arrow_forward,color:Colors.lightBlue))
```
4. Wrap the Column in a Container having this properties
      margin: EdgeInsets.all(16.0),
      padding: EdgeInsets.all(16.0),
      decoration: BoxDecoration(
      color: Color.fromARGB(255, 35, 11, 63),
      border: Border.all(),
      borderRadius: BorderRadius.all(Radius.circular(3.0))
```dart
Container( margin: EdgeInsets.all(16.0),
        padding: EdgeInsets.all(16.0),
        decoration: BoxDecoration(
          color: Color.fromARGB(255, 35, 11, 63),
          border: Border.all(),
          borderRadius: BorderRadius.all(Radius.circular(3.0))),
          child:Column(mainAxisSize: MainAxisSize.min,...
```
6. Change the color of text to White using TextStyle
```dart
Text("FLUTTER",style: TextStyle(color: Colors.white)
```
7. Add BottomBarNavigation to Scaffold with3 icons
```dart
bottomNavigationBar: BottomNavigationBar(
        items: const <BottomNavigationBarItem>[
          BottomNavigationBarItem(
            icon: Icon(Icons.home),
            label: 'Home',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.business),
            label: 'Business',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.school),
            label: 'School',
          ),
        ],
        currentIndex: 0,
        selectedItemColor: Colors.purple[900],
        ),
```
## Exercice 2
the purpose of this activity is to do with ListView
1. Create a new Widget ListLayout with MaterialApp et Scaffold as widget Root
2. in the body of scaffold, Display a Listview with three Text A,B, C 
```dart
ListView(children: [Text("A"),Text("B"),Text("C")],padding: EdgeInsets.all(8),)
```
3. place each Text in a container with a background color that you choose and a height of 50
```dart
ListView(children: [Container(child: Text("A"),height:50,color: Colors.amber,),Container(child:Text("B"),height:50,color: Colors.amber[100],),Container(child:Text("C"),height:50,color: Colors.amber[200],)],padding: EdgeInsets.all(8),)
```
4. place each Text in the center of container using the widget Center
the result will be like this </br>
<img src=""/>
