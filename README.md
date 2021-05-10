import 'package:flutter/material.dart';

void main() => runApp(new UssdApp());

class UssdApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: "USSDapp",
      theme: ThemeData(
        primaryColor: const Color(0xff2980b9), // AARRGGBB
      ),
      home: new LoginAppStateful(),
    );
  }
}

class LoginAppStateful extends StatefulWidget {
  LoginApp createState() => LoginApp();
}

class LoginApp extends State<LoginAppStateful> {
  Widget build(BuildContext cx) {
    return new Scaffold(
        appBar: null,
        body: new Container(
          decoration: BoxDecoration(
            gradient: LinearGradient(
              colors: [
                const Color(0xFF3A3D3E),
                const Color(0xFFFFFFFF),
              ],
              begin: Alignment.centerLeft,
              end: Alignment(-1.0, -1.0),
            ),
          ),
          height: 380.0,
          child: Column(
            mainAxisAlignment: MainAxisAlignment.start,
            children: <Widget>[
              Container(
                child: Image(
                  image: AssetImage("images/provider_logo.png"),
                  height: 300.0,
                  width: double.infinity,
                ),
                margin: EdgeInsets.all(20.0),
              ),
              Column(
                children: [
                  Card(
                    margin: EdgeInsets.all(10),
                    elevation: 8,
                    child: Container(
                      padding: EdgeInsets.all(25),
                      child: Text(
                        'beeline',
                        style: TextStyle(color: Colors.green),
                      ),
                    ),
                  ),
                  SizedBox(
                    width: 4,
                  ),
                  Card(
                    margin: EdgeInsets.all(10),
                    elevation: 8,
                    child: Container(
                      padding: EdgeInsets.all(25),
                      child: Text(
                        'uzmobile',
                        style: TextStyle(color: Colors.green),
                      ),
                    ),
                  ),
                ],
              )
            ],
          ),
        ),
    );
  }
}
