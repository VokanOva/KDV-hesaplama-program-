import java.util.Scanner;
public class KDV {
    public static void main(String[] args) {
        double tutar, kdvOran, kdvTutar, kdvliTutar;

        Scanner input = new Scanner(System.in);
        System.out.print("Tutari Miktari: ");
        tutar = input.nextDouble();

        boolean fiyat1 = tutar < 1000;
        boolean fiyat2 = tutar >= 0;
        kdvOran = fiyat1 && fiyat2 ? 0.08 : 0.18;

        kdvTutar = tutar * kdvOran;
        kdvliTutar = tutar + kdvTutar;

        System.out.println("KDV'siz Tutar: "+ tutar);
        System.out.println("KDV Oran: "+ kdvOran );
        System.out.println("KDV Tutari: "+ kdvTutar);
        System.out.println("KDV'li Tutari: "+ kdvliTutar);
