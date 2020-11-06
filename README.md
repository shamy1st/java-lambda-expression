# Lambda Expression
**Lambda Expression** is an implementation of functional interface like anonymous inner class implementation.

        Printer printer = message -> System.out.println(message);
        printer.print("Hello Lambda Expression!");

**Instead of**

        public class Main {
            public static void main(String[] args) {
                sayHello(new Printer() {
                    @Override
                    public void print(String message) {
                        System.out.println(message);
                    }
                });
            }

            public static void sayHello(Printer printer) {
                printer.print("Hello");
            }
        }
