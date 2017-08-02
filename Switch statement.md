#Switch statement
rules and an example.
```java
/**
*variable in a switch statment can only be integers,convertavle integers(btye,short,char).string and enums(days of the week).
*a value for a case must be constant or literal.
*a break statement should be in the end of the case statement.
*a default statement is optional.
*/
class Transcript{
    String grade;

    Transcript(int score){
        this.grade = transScore(score);
        System.out.println("Grade is "+grade);
    }

    private String transScore(int score){
        String grade = new String();

        switch(score){
            case(90): grade = "A";break;
            case(80): grade = "B";break;
            default: grade = "F";
        }

        return grade;
    }

    public static void main(String[] args){
        Transcript trans1 = new Transcript(90); 
    }
}
```java