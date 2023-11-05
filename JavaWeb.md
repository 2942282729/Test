# Java Web Study

## One: How to build a Maven project?

1. Select org. apache. maven. archetypes :maven-archetype -web app 

   ![image-20231027145616866](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145616866.png)

   

2.  Set local maven storage warehouse

   ![image-20231027145718356](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145718356.png)
   
3. Right-click in the main directory to complete the java and resource directories

   ![image-20231027145726882](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145726882.png)

   

4. Here is the result image after adding the directories

   ![image-20231027145733763](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145733763.png)
   



## Two: How to integrate tomcat with our maven project?

### One Way: Add local Tomcat

1. We need to click Edit Configurations

   ![image-20231027145742126](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145742126.png)
   
2. Then add Local Tomcat

   | <img src="C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145834210.png" alt="image-20231027145834210" style="zoom:150%;" /> | <img src="C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145843923.png" alt="image-20231027145843923" style="zoom:150%;" /> |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |

   

3. Click Deployment option then Click Artifact

   ![image-20231027145945144](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145945144.png)
   
4. Choose Your project name::war

   ![image-20231027145952630](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145952630.png)
   
5. The 'application context' is the access path for our project, we're able to change it but now we use default. Click 'apply' and then ok.

   ![image-20231027150015834](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150015834.png)

   

6. Now we can see that Tomcat has been integrated with our project


   ![image-20231027150030263](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150030263.png)

   

7. Create an html file in the web app directory 

   ![image-20231027150038346](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150038346.png)

   

8. We can click the green arrow to run our project using the Tomcat server

   ![image-20231027150045708](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150045708.png)

   

9. Now we can see that Tomcat successfully runs our project file！

   ![image-20231027150052834](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150052834.png)

   


### Another Way: Import Tomcat plugins

1. Use the shortcut alt+insert in the pom.xml file.

   ![image-20231027145510009](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027145510009.png)
   
2. Choose Plugin Template, then enter the content

   ```xml
   <build>
   	<!--Tomcat插件-->
   	<plugins>
   	<plugin>
   	<groupId>org.apache.tomcat.maven</groupId>
   	<artifactId>tomcat7-maven-plugin</artifactId>
   	<version>2.2</version>
   	</plugin>
   	</plugins>
   </build>
   ```

   

3. Now we can use Tomcat7:run to run our own web project!

   ![image-20231027150247098](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150247098.png)

## Three: How to build a Servlet?

1. First we need to create a new web project as we did before, and then import the dependency coordinates for the Servlet into the pom.xml.

   

   ```xml
   <dependencies>
   
   <!--tomcat插件-->
   
   <dependency>
   
   <groupId>org.apache.tomcat.maven</groupId>
   
   <artifactId>tomcat7-maven-plugin</artifactId>
   
   <version>2.2</version>
   
   </dependency>
   
    
   
   <!--Servlet坐标-->
   
   <dependency>
   
   <groupId>javax.servlet</groupId>
   
   <artifactId>javax.servlet-api</artifactId>
   
   <version>3.1.0</version>
   
   <scope>provided</scope>
   
   </dependency>
   
   
   </dependencies>
   ```

   

   

   ![image-20231027150732615](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150732615.png)

   

   

2. Create a new java class

   ![image-20231027150858811](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150858811.png)

3. Here is the initial Java Class

   ![image-20231027150907530](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027150907530.png)
   
4. We must add some code to implement Servlet Class and then configure the annotations for the Web Servlet to provide the access path 

   - Implements a Servlet Class

     

   ![image-20231027151213534](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027151213534.png)

    

   - Implement every functions in Servlet Class

     Use the shortcut alt+insert 

   ![image-20231027151226589](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027151226589.png)

   

   - The results are as follows

   ![image-20231027151236142](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027151236142.png)

   

   - configure the annotations for the Web Servlet 

   ![image-20231027151251690](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027151251690.png)

   

5. Run Tomcat service then enter the configured address in the browser address bar, we can see " Hello Servlet" was exported in Java Console.


![image-20231027151301520](C:\Users\haoChen\AppData\Roaming\Typora\typora-user-images\image-20231027151301520.png)

