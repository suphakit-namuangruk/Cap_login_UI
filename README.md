import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  
  const MyApp({Key? key}) : super(key: key);
  static const String _title = '';

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: _title,
      home: Scaffold(
        body: const MyStatefulWidget(),
      ),
    );
  }
}

class MyStatefulWidget extends StatefulWidget {
  const MyStatefulWidget({Key? key}) : super(key: key);

  @override
  State<MyStatefulWidget> createState() => _MyStatefulWidgetState();
}

class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  TextEditingController nameController = TextEditingController();
  TextEditingController passwordController = TextEditingController();

  @override
  Widget build(BuildContext context) {
    return Padding(
        padding: const EdgeInsets.all(10),
        child: ListView(
          children: <Widget>[
            Container(
              margin: const EdgeInsets.only(top: 56.0),
              alignment: Alignment.center,
              child: Image.asset(
                'assets/images/Logo.png',
                height: 90,
                width: 90,
              ),
            ),
            Container(
                alignment: Alignment.center,
                padding: const EdgeInsets.all(10),
                child: const Text(
                  'Welcome to Passi',
                  style: TextStyle(
                      color: Color(0xFF3B4C7A),
                      fontWeight: FontWeight.w700,
                      fontSize: 24),
                )),
            Container(
                alignment: Alignment.center,
                padding: const EdgeInsets.only(top: 3.0),
                child: const Text(
                  'Welcome Back!',
                  style: TextStyle(
                      color: Color(0xFF4F4F4F),
                      fontWeight: FontWeight.w400,
                      fontSize: 16),
                )),
            Container(
                alignment: Alignment.center,
                padding: const EdgeInsets.only(top: 0.0),
                child: const Text(
                  'Please enter your details!',
                  style: TextStyle(
                      color: Color(0xFF4F4F4F),
                      fontWeight: FontWeight.w400,
                      fontSize: 16),
                )),
            Container(
                alignment: Alignment.centerLeft,
                padding: const EdgeInsets.only(top: 32.0, left: 10.0),
                child: const Text(
                  'Email',
                  style: TextStyle(
                      color: Color(0xFF3B4C7A),
                      fontWeight: FontWeight.w600,
                      fontSize: 16),
                )),
            Container(
              padding: const EdgeInsets.all(10),
              child: TextField(
                controller: nameController,
                decoration: const InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'Email',
                ),
              ),
            ),
            
            Container(
                alignment: Alignment.centerLeft,
                padding: const EdgeInsets.only(top: 5.0, left: 10.0),
                child: const Text(
                  'Password',
                  style: TextStyle(
                      color: Color(0xFF3B4C7A),
                      fontWeight: FontWeight.w600,
                      fontSize: 16),
                )),
            Container(
              alignment: Alignment.centerLeft,
              padding: const EdgeInsets.only(top: 5.0, left: 10.0),
              child: TextField(
                obscureText: true,
                controller: passwordController,
                decoration: const InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'Password',
                ),
              ),
            ),
            Container(padding: const EdgeInsets.only(top: 32.0)),
            ElevatedButton(
              onPressed: () {},
              child: const Text('Sign In'),
              style: ButtonStyle(
                backgroundColor: MaterialStateProperty.all(Color(0xFF5771DF)),
                minimumSize: MaterialStateProperty.all(const Size(332, 36)),
              ),
            ),
            Container(
              alignment: FractionalOffset.bottomCenter,
              child: Row(
                children: <Widget>[
                  const Text('Not have an accout?',
                      style: TextStyle(
                        fontSize: 14,
                        color: Color(0xFF4F4F4F),
                        fontWeight: FontWeight.w300,
                      )),
                  TextButton(
                    child: const Text(
                      'Create One.',
                      style: TextStyle(
                        fontSize: 14,
                        color: Color(0xFF5771DF),
                        fontWeight: FontWeight.w300,
                      ),
                    ),
                    onPressed: () {
                      //signup screen
                    },
                  )
                ],
                mainAxisAlignment: MainAxisAlignment.center,
              ),
            ),
          ],
        ));
  }
}
