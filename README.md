# giris

import java.util.Scanner;

public class kullanicigiris {

    public static void main(String[] args) {

        String userName, passWord,sifirlendirme, newPassword ;
        Scanner input= new Scanner(System.in);
        System.out.print(" Kullanci adınızı yazınız: ");
        userName=input.nextLine( );
        System.out.print(" Şifrenizi yazınız: ");
        passWord=input.nextLine();

        if (userName.equals("patika") && passWord.equals("java") ){
            System.out.println(" ***  Başarılı bir şekilde giriş yaptınız. **** ");

        }
        else{
            System.out.println("  Hatali şifre girdiniz yeni şifre belirtmek isterseniz \"evet\"  istemezseniz \" hayir\"  seçin: ");
            sifirlendirme=input.nextLine();

            if( sifirlendirme.equals("hayir")){
                System.out.println("Giris sonlandırıldı. ");}

            else if (sifirlendirme.equals("evet")) {
                System.out.println("Yeni Şifre: ");
                newPassword=input.nextLine();

                if( newPassword.equals("java")|| newPassword.equals(passWord)){
                    System.out.println("Şifre oluşturulamadı, lütfen başka şifre giriniz.");
                    newPassword=input.nextLine();
                    if (!newPassword.equals("java")) {
                        System.out.println("Yeni Şifre oluşturuldu.");
                    }
                        else {
                            System.out.println("Girdiğiniz şifre unutmuş olduğunuz şifre ile aynıdır. Yeni şifre giriniz: ");
                            newPassword = input.nextLine();
                            System.out.println("Şifreniz başarılı bir şekilde oluşturuldu.");
                    };


                }
                else{
                    System.out.println("Şifre oluşturuldu.");
                }
            }
            else{
                System.out.println("Hatali seçim yaptınız.");

            }

        }
    }

}
