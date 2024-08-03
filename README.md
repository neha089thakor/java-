# java-public class Main {

    public static void main(String[] args) {
        double doubleValue = 9.78;
        int intValue;
        intValue = (int) doubleValue;

        System.out.println("Original double value: " + doubleValue);
        System.out.println("Value after casting to int: " + intValue);
        class Animal {
            void makeSound() {
                System.out.println("Animal makes a sound");
            }
        }


        class Dog extends Animal {
            void bark() {
                System.out.println("Dog barks");
            }
        }


        Animal myAnimal = new Dog();


        Dog myDog = (Dog) myAnimal;

        myAnimal.makeSound();
        myDog.bark();


        try {

            Animal anotherAnimal = new Animal();
            Dog wrongCast = (Dog) anotherAnimal;
        } catch (ClassCastException e) {
            System.out.println("ClassCastException occurred: " + e.getMessage());
        }
    }
}
