# Lambda Expression
**Lambda Expression** is an implementation of functional interface like anonymous inner class implementation.

        Printer printer = message -> System.out.println(message);
        printer.print("Hello Lambda Expression!");

**Instead of**

**1. Interface Implementation**

        public class Main {
            public static void main(String[] args) {
                Printer printer = new PrinterImpl();
                printer.print("Hello");
            }
        }

        public interface Printer {
            void print(String message);
        }

        public class PrinterImpl implements Printer {
            @Override
            public void print(String message) {
                System.out.println(message);
            }
        }

**2. Anonymous Class**

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
