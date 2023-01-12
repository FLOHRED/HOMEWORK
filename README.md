# HOMEWORK
public class MyClass {
    public static void main(String[] args) {
    SmartDevice telefono = new SmartDevice(); 
    telefono.color = "Rojo";
    System.out.println(telefono.color);
    SmartPhone phone =new SmartPhone("xfd", "azul", 60, 9, 16, "Z", "Samsung");
        System.out.println(phone.fabricante);
    SmartWatch watch = new SmartWatch("tyu","yellow", 40, 30, 12, 2021);    
        System.out.println(watch.año);

    }
    
    public static class SmartDevice {
        String modelo;
        String color;
        int peso;
        int ampersBateria;
        int memoria;
        
    public SmartDevice(){}
        

    public SmartDevice(String modelo, String color, int peso, int ampersBateria, int memoria){
        
        this.modelo = modelo;
        this.color = color;
        this.peso = peso;
        this.ampersBateria = ampersBateria;
        this.memoria = memoria;
    }
    }
    
    public static class SmartPhone extends SmartDevice {
        
        String generacion;
        String fabricante;
        
    public SmartPhone(String modelo, String color, int peso, int ampersBateria, int memoria, String generacion, String fabricante) {
        super(modelo, color, peso, ampersBateria, memoria);
        this.generacion = generacion;
        this.fabricante = fabricante;
    }
    }
    
   public  static class SmartWatch extends SmartDevice {
       int año;
             
  public SmartWatch(String modelo, String color, int peso, int ampersBateria, int memoria, int año) {
          super(modelo, color, peso, ampersBateria, memoria);
        this.año = año;
  }
   }
}
