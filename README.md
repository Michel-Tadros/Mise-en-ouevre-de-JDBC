# Mise-en-ouevre-de-JDBC
### Softwares utilisés:
1. IDE : IntelliJ Idea 2021.2.1 
2. Database Type: Mysql
3. Driver : mysql-connector.jar

## Démarche suivie:
- Créer d'une nouvelle database nommée javadb: `create database javadb;` 
- Créer d'une table employe: `create table employe(id int(10),name varchar(40),age int(3));`
- Insérer dans la table 2 éléments.  ![image](https://user-images.githubusercontent.com/89968019/151579939-0520e2b3-58ed-4d89-af25-0a3625171338.png)
- Utiliser le driver de type mysql: "com.mysql.jdbc.Driver".
- Utiliser l'URL suivant pour se connecter au databse: "jdbc:mysql://localhost:3306/javadb","root","".
- Télécharger mysql-connector.jar.
- L'insérer dans le projet IntelliJ en cliquant sur File->Project Structure->Libraries->+->ajouter mysql-connector.jar ![image](https://user-images.githubusercontent.com/89968019/151581620-bfd8b50b-3c68-4f89-a9a7-d8f2dfe04359.png)
- Pour pouvoir se connecter a une mysql database et envoyer des requetes sql dans java : `import java.sql.*;`.
- Créer une connection: `Connection con=DriverManager.getConnection("jdbc:mysql://localhost:3306/javadb","root","")`.
- Créer un statement: `Statement stmt=con.createStatement();`.
- Créer un query : `ResultSet rs=stmt.executeQuery("select * from employe");`.
- Afficher le résultat de la requete : `while(rs.next()) System.out.println(rs.getInt(1)+"  "+rs.getString(2)+"  "+rs.getString(3));`.
- Exécuter le programme.
- Output : ![image](https://user-images.githubusercontent.com/89968019/151582655-b2c41a13-b72a-4e81-9f41-662ec4ed0ed6.png)
  

