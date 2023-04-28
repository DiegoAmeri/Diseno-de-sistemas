http://localhost:65215/?code=bce2bfb14b17121be61b&state=3187fc96a6c042bca234fcdb904601e3 url desa

package desarrollo;

import java.util.ArrayList;
import java.util.Scanner;

public class RegisterGuia {
    public static void main(String[] args) {
        ArrayList<String> guias = new ArrayList<>(); // Creamos un ArrayList para almacenar las guías
        String usuario = "usuario"; // Usuario para la sesión
        String password = "contraseña"; // Contraseña para la sesión

        Scanner scanner = new Scanner(System.in);

        // Ciclo para permitir el inicio de sesión
        while (true) {
            System.out.println("Ingrese su usuario: ");
            String usuarioIngresado = scanner.nextLine();

            System.out.println("Ingrese su contraseña: ");
            String contraseñaIngresada = scanner.nextLine();

            if (usuarioIngresado.equals(usuario) && contraseñaIngresada.equals(password)) { // Verificamos que el
                                                                                            // usuario y contraseña sean
                                                                                            // correctos
                System.out.println("Sesión iniciada correctamente.");
                break;
            } else {
                System.out.println("Usuario o contraseña incorrectos. Intente nuevamente.");
            }
        }

        // Ciclo para permitir múltiples operaciones
        while (true) {
            System.out.println("Ingrese la operación que desea realizar (A: alta, B: baja, M: modificación): ");
            String operacion = scanner.nextLine().toUpperCase(); // Convertimos a mayúsculas para simplificar la
                                                                 // validación

            if (operacion.equals("A")) { // Operación de alta
                System.out.println("Ingrese el número de guía: ");
                String guia = scanner.nextLine();
                guias.add(guia); // Agregamos la guía al ArrayList
                System.out.println("La guía " + guia + " ha sido registrada.");
            } else if (operacion.equals("B")) { // Operación de baja
                System.out.println("Ingrese el número de guía a eliminar: ");
                String guia = scanner.nextLine();
                if (guias.remove(guia)) { // Verificamos si se eliminó la guía
                    System.out.println("La guía " + guia + " ha sido eliminada.");
                } else {
                    System.out.println("La guía " + guia + " no existe.");
                }
            } else if (operacion.equals("M")) { // Operación de modificación
                System.out.println("Ingrese el número de guía a modificar: ");
                String guiaAntigua = scanner.nextLine();
                System.out.println("Ingrese el nuevo número de guía: ");
                String guiaNueva = scanner.nextLine();
                int indice = guias.indexOf(guiaAntigua);
                if (indice != -1) { // Verificamos si existe la guía a modificar
                    guias.set(indice, guiaNueva);
                    System.out.println("La guía " + guiaAntigua + " ha sido modificada por " + guiaNueva + ".");
                } else {
                    System.out.println("La guía " + guiaAntigua + " no existe.");
                }
            } else {
                System.out.println("Operación no válida. Intente nuevamente.");
            }
        }
    }
}


package desarrollo;

public class RegisterReserva {

}


package desarrollo;

public class RegisterReserva {

}

