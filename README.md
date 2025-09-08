/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package Lab2_SahelAssadi;




import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;
import javafx.scene.image.*;
import java.util.Random;
import javafx.geometry.Insets;


/**
 *
 * @author 6321596
 */
public class Lab2 extends Application {


    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        launch(args);
    }


    @Override
    public void start(Stage primaryStage) {
        BorderPane root = new BorderPane();
        primaryStage.setTitle("Java Games");
        Label top = new Label("Random Game");
        root.setTop(top);
        Label bottom = new Label("Waiting...");
        root.setBottom(bottom);
        Label rightLabel = new Label();
        BorderPane.setMargin(rightLabel, new Insets (10, 10, 10, 10));
        Label leftLabel = new Label();
        BorderPane.setMargin(leftLabel, new Insets (10, 10, 10, 10));


        Label imagelabel = new Label();
        VBox vb = new VBox(imagelabel);
        root.setCenter(vb);
        Random random = new Random();
        int randomNum = random.nextInt(20) + 101;
        Image image = new Image("file:src/images/" + randomNum + ".jpg");
        ImageView imageView = new ImageView(image);
        imagelabel.setGraphic(imageView);
        Scene scene = new Scene(root, 250, 300);
        primaryStage.setScene(scene);
        primaryStage.show();


    }


}
 
