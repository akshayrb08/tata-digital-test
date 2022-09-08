1. Refactor code to wrap children to next line
A ->
     class LongStringWidget extends StatelessWidget {
      const LongStringWidget({Key? key}) : super(key: key);

      @override
      Widget build(BuildContext context) {
        return Wrap(
          children: const [
            Chip(label: Text('I')),
            Chip(label: Text('am')),
            Chip(label: Text('looking')),
            Chip(label: Text('for')),
            Chip(label: Text('a')),
            Chip(label: Text('job')),
            Chip(label: Text('and')),
            Chip(label: Text('I')),
            Chip(label: Text('need')),
            Chip(label: Text('a')),
            Chip(label: Text('job')),
          ],
        );
      }
    }


2. Identify problem in code block and correct it.
A ->
      Future<String> longOperationMethod()async{
        var counting =0;
        for (var i=1;i<=1000000000;i++){
          counting=i;
        }
        return Future.value('$counting! I print the value!');
      }
      To get the return value, we can call function like below,
      longOperationMethod().then((value) => print(value));



3. Difference between these lists and will the last 2 lines compile?
A -> 1.const list3=list1; - will not compile as list1 is not a const value
     2.list2[2]='Dart'; - will compile only if 1 is removed/commented else compiler will fail.