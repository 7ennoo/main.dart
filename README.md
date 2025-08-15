import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.black87,
        body: Center(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              TextWidget('Hello Flutter'), 
              const SizedBox(height: 20),         
              BackgroundWidget(Colors.blue),
            ],
          ),
        ),
      ),
    );
  }
}


class MyBaseWidget extends StatelessWidget {
  final Widget child;
  const MyBaseWidget({required this.child, super.key});

  Widget build(BuildContext context) {
    return Center(child: child);
  }
}


class TextWidget extends MyBaseWidget {
  TextWidget(String text)
      : super(
          child: Text(
            text,
            style: const TextStyle(
              fontSize: 24,
              color: Colors.white,
            ),
          ),
        
class BackgroundWidget extends MyBaseWidget {
  BackgroundWidget(Color color)
      : super(
          child: Container(
            width: 200,
            height: 200,
            decoration: BoxDecoration(
              color: color,
              borderRadius: BorderRadius.circular(20),
          ),
        ),
      );
}
