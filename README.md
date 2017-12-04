# android_learning
the first step of Android

2017/12/4

ArrayAdapter的应用
在学习Android的控件ListView时，《第一行代码》p114有如下代码：
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ArrayAdapter<String> adapter =new ArrayAdapter<String>(
                MainActivity.this,android.R.layout.simple_list_item_1,data);

        ListView listView = (ListView)findViewById(R.id.list_view);
        listView.setAdapter(adapter);


    }
因为数组的数据无法直接传给ListView所以需要借助适配器，这里采用ArrayAdapter适配器，适配通过泛型来指定适配的数据类型，传入的是字符串，则为
                                                                                                                        ArrayAdapter<String> 
然后在ArrayAdapter的构造函数中传入上下文（有点类似Intent），ListView的子项的id，代码中的android.R.layout.simple_list_item1作为ListView的子布局,
在使用了ArrayAdapter适配器后，还要调用ListView的setAdapter方法。
