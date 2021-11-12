# tanlovli-mashq-
late int type;
void main() {
  List list = [
    Student(50, "Javlon", false,'M'),
    Student(20, "Xurshid", true,'M'),
    Student(30, "Laali", false,'F'),
    Student(40, "xaali", true, 'F')
           ];

  type = 4;
  list.sort();
  print(list);
}

void doFilterBy(int type, List list) {}

class Student implements Comparable {
  int userId;
  String name;
  bool active;
  String char= '';
  Student(this.userId, this.name, this.active,this.char);

  @override
  String toString() {
    return '{$userId, $name, $active,$char}';
  }

  @override
  int compareTo(other) {
    if (type == 1) {
      return (userId.compareTo(other.userId));
    } else if (type == 2) {
      return (name.compareTo(other.name));
    } else if(type == 4){
      return (-char.compareTo(other.char));
    } else{
      if (active == true) {
        return -1;
      }
      return 1;
    }
  }
}
