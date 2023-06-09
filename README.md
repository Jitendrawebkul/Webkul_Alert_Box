
<<<<<<< HEAD
=======
 
# Webkul Alert Box

Fancy container package lets you add a beautiful gradient container to your Flutter app.

## Installation 

1. Add the latest version of package to your pubspec.yaml (and run`dart pub get`):
```yaml
dependencies:
  flutter_webkul_alert_box: ^0.0.1
```
2. Import the package and use it in your Flutter App.
```dart
import 'package:fancy_containers/WebkulDialog.dart';
```


<hr>

<table>
<tr>
<td>

```dart
class WebkulAlertClass extends StatelessWidget {
   @override
   Widget build(BuildContext context) {
     return Scaffold(
       body: Center(
         child: Container(
              child: TextButton(
                  style: ButtonStyle(
                    foregroundColor: MaterialStateProperty.all<Color>(Colors.blue),
                    overlayColor: MaterialStateProperty.resolveWith<Color?>(
                          (Set<MaterialState> states) {
                        if (states.contains(MaterialState.hovered))
                          return Colors.blue.withOpacity(0.04);
                        if (states.contains(MaterialState.focused) ||
                            states.contains(MaterialState.pressed))
                          return Colors.blue.withOpacity(0.12);
                        return null; // Defer to the widget's default.
                      },
                    ),
                  ),
                  onPressed: () {
                    showDialog(
                      context: context,
                      builder: (ctx) => WebkulDialouge(
                        icon: Icon(
                          Icons.add_alert,
                          color: Colors.teal,
                          size: 80.0,
                        ),
                        title: 'Add to cart',
                        message: 'Product added to cart successfully',
                        actions: [
                          TextButton(
                            onPressed: () => Navigator.of(ctx).pop(),
                            child: Text('OKAY'),
                            style: TextButton.styleFrom( //<-- SEE HERE
                              side: BorderSide(width: 2.0, color: Colors.black),
                            ),
 
                          ),
                        ],
                      ),
                    );
                  },
                  child: Text('Open Webkul Alert')
              ),
         ),
       ),
     );
   }
 }

```

>>>>>>> d86824b (readme.md file details added)
