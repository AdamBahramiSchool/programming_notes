## Dynamic Array Behavior ## 

import java.util.Arrays;

public class Array {
    private int count;
    private int[] arr;
    private int size;
    Array() {
        this.size=5;
        this.arr = new int [this.size];
        fill_array();
    }

    public void fill_array(){
        for(int i=0;i<this.size;i++){
            this.arr[i]=i;
            this.count+=1;
        }
    }

    public void push_array(int num){
//        you have static array that's full. if pushing to it, and size is full, create new array double the size and copy original in
        if(this.count==(this.size)){
            int[] new_arr = new int[this.size*2];
            for(int i=0; i<this.size;i++){
                new_arr[i]=this.arr[i];
            }
            this.arr=new_arr;
            this.size=this.size*2;
        }
        this.arr[this.count]=num;
        this.count+=1;

    }

    public void display_array(){
        System.out.println(Arrays.toString(this.arr));
    }
}

