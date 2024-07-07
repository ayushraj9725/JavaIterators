# JavaIterators
import java.util.ArrayList;
import java.util.Iterator;

public class IterableLists {
    public static void main(String args[]){
        ArrayList<String> name = new ArrayList<>();

        name.add("ayush");
        name.add("aaditya");
        name.add("anushka");

        System.out.println(name);

        System.out.println(name.size()); // this size will veary that mean  it is defind  dynamically tells size of list 

        System.out.println(name.contains("ayush")); // if ayush exist in name list then it return true otherwise false

        // now we are iterating the name list 
        // 1 way to use simple for loop and iterate 

        for(int i = 0 ; i < name.size() ;i++){
            System.out.println("name is : "+name.get(i)+ " at index "+i);
        }

        //2nd way to iterating the name list is for each way 
        System.out.println("by for each method ");

        for(String thisname : name){
            System.out.println("name is : "+thisname);
        }

        // 3rd way to iterate using iterator it implement like this
        System.out.println("by using Iterator ");
        
        Iterator<String> st = name.iterator(); //Iterator has many functionalitis which helps to iterate the list 
                                               // it returns an iterator over the elements in the list in proper sequence by traverse list
        while(st.hasNext()){
            System.out.println("Iterator : "+st.next()); // hasNext() method check items exist in list or no by moveing to next
        }                                               // next() method used to access that existing items in the list
    }    
}
