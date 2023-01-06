# pub-dev-time-intervals


<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages).
-->

This package can create a time interval of list in map of [from and to]
means it can create a gap nof time or break the time in small time intervals.  

## Features

1. you can get time interval in list of map .

2. you can get time interval in TimeOfDate formate.

3. This include null safty also.


## Getting started

 - To use this you must have 
 
 [*] starting time (in TimeOfDate)
 [*] ending time (in TimeOfDate)
 [*] gap time from (in TimeOfDate)
 [*] gap time to (in TimeOfDate)
 [*] interval (in int)

== Now, Just call generateTimeIntervals ==

## Usage

```dart
List<Map<String,TimeOfDay>>? timing;
 
  // --- Services timing ---
   TimeOfDay _openingTime = const TimeOfDay(
    hour: 08,
    minute: 00,
  );
  TimeOfDay _closingTime = const TimeOfDay(
    hour: 16,
    minute: 00,
  );
  TimeOfDay _lunchTimeTo = const TimeOfDay(
    hour: 14,
    minute: 00,
  );
  TimeOfDay _lunchTimeFrom = const TimeOfDay(
    hour: 13,
    minute: 00,
  );
  int _avgTime = 10;

 @override
  void initState() {
    // TODO: implement initState
    getIntervalOfServices();
    super.initState();
  }

 void getIntervalOfServices(){
  timing =  generateTimeIntervals(avgTime: _avgTime,closingTime: _closingTime,openingTime: _openingTime,lunchTimeFrom: _lunchTimeFrom,lunchTimeTo: _lunchTimeTo ); 
 }

  Container(
            width: size.width,
            height: 200 ,
            padding: const EdgeInsets.symmetric(vertical: 8.0),
            decoration: const BoxDecoration(
            color: Colors.white,
              boxShadow: [
               BoxShadow(
              offset: Offset(0.0, 2.5),
              blurRadius: 3.5,
              color: Colors.black54,
              )
              ]
            ),
            child: GridView.builder(
              itemCount: timing.length,
              gridDelegate: const SliverGridDelegateWithFixedCrossAxisCount(
                crossAxisCount: 4,
                crossAxisSpacing: 0.5,
                mainAxisSpacing: 0.5,
                 childAspectRatio: 2.5,
                ),
              scrollDirection: Axis.vertical,
              itemBuilder: (context, index) => Chip(label:  Text(
            "${timing[index]["from"].format(context)}-${timing[index]["to"].format(context)}",
            style: const TextStyle(fontSize: 8.0),
          ),padding: const EdgeInsets.only(left:0,right:0),elevation: 1.5,backgroundColor: const Color.fromARGB(133, 237, 236, 236), ),
            ),
          );
 
```
# Examples -

### Example 1 -
![alt loading](image1.png)

### Example 1 -
![alt loading](image2.png)

### Example 1 -
![alt loading](image3.png)

### Example 1 -
![alt loading](image4.png)

### Example 1 -
![alt loading](image5.png)

## Additional information

This package can create a time interval of list in map of [from and to]
means it can create a gap nof time or break the time in small time intervals.
