# main
```markdown
import 'package:flutter/material.dart';
import 'package:testapp/widgets/video_card.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Actividad en Flutter',
      debugShowCheckedModeBanner: false,
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: MyWidget(),
    );
  }
}

class MyWidget extends StatelessWidget {
  const MyWidget({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: const Text("Reproductor"),
          backgroundColor: Colors.purple,
          actions: const [
            Icon(Icons.search),
            Icon(Icons.camera_front),
            Icon(Icons.person),
          ],
        ),
        body: const SingleChildScrollView(
            child: Column(
                children: const [VideoCard(), VideoCard(), VideoCard()])));
  }
}

```
# video_card
```markdown
import 'package:flutter/material.dart';

class VideoCard extends StatelessWidget {
  const VideoCard({super.key});

  @override
  Widget build(BuildContext context) {
    return Padding(
      padding: const EdgeInsets.all(15.0),
      child: Column(
        children: [
          Container(
            child: Image.asset("assets/images/test.png"),
          ),
          const SizedBox(
            height: 5,
          ),
          Row(
            children: [
              const CircleAvatar(
                radius: 25,
                backgroundImage: AssetImage("assets/images/test.png"),
              ),
              const SizedBox(
                width: 15,
              ),
              Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Container(
                    width: 250,
                    child: const Text(
                      "Titulo del video",
                      style:
                          TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
                    ),
                  ),
                  const Text(
                    "Tec    -50 Views",
                    style: TextStyle(fontSize: 15),
                  )
                ],
              )
            ],
          )
        ],
      ),
    );
  }
}

```
