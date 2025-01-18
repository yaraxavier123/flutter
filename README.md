# flutter
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Layout Responsivo'),
        ),
        body: LayoutBuilder(
          builder: (context, constraints) {
            if (constraints.maxWidth < 600) {
              return Column(
                children: [
                  Text('Tela Pequena'),
                  // Adicione mais widgets aqui
                ],
              );
            } else {
              return Row(
                children: [
                  Text('Tela Grande'),
                  // Adicione mais widgets aqui
                ],
              );
            }
          },
        ),
      ),
    );
  }
}
