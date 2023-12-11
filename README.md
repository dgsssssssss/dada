using System;
using System.Collections;
class Program {
  static void Main(string[] args) {
    //  Zadanie 1
    int[] numbers = { 4, 7, 2, 8, 5 };
    int numberToFind = 2;
    int index = FindIndex(numbers, numberToFind);
    Console.WriteLine("Index of the number in the array: " + index);
    //  Zadanie 2
    ArrayList list = new ArrayList() { 4, 7, 2, 8, 5 };
    int elementToFind = 7;
    int indexInList = FindIndexInArrayList(list, elementToFind);
    Console.WriteLine("Index of the element in the list: " + indexInList);
    //  Zadanie 3
    ArrayList menuList = new ArrayList();
    while (true) {
      Console.WriteLine("Menu:");
      Console.WriteLine("1. Dodaj");
      Console.WriteLine("2. Usuń");
      Console.WriteLine("3. Wyświetl");
      Console.WriteLine("4. Zakończ");
      string option = Console.ReadLine();
      if (option == "1") {
        Console.WriteLine("Podaj element do dodania:");
        string element = Console.ReadLine();
        menuList.Add(element);
      } else if (option == "2") {
        Console.WriteLine("Podaj element do usunięcia:");
        string element = Console.ReadLine();
        menuList.Remove(element);
      } else if (option == "3") {
        Console.WriteLine("Zawartość listy:");
        foreach (var item in menuList) {
          Console.WriteLine(item);
        }
      } else if (option == "4") {
        Console.WriteLine("Do zobaczenia");
        break;
      }
    }
  }
  // Zadanie 1
  static int FindIndex(int[] arr, int num) {
    for (int i = 0; i < arr.Length; i++) {
      if (arr[i] == num) {
        return i;
      }
    }
    return -1;
  }
  // Zadanie 2
  static int FindIndexInArrayList(ArrayList list, int num) {
    return list.IndexOf(num);
  }
}
