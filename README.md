android-fly-in-app-navigation
=============================

This project serves as a way to implement the fly-in app navigation seen in apps like Facebook, Evernote, and Prixing.

Adding this project to your list of libraries will give you access to a new class, FanView. FanView contains two user-defined layouts that it uses to make this UI pattern. You can define the two layouts seperately just like you would define a regular layout. You then just specifiy the id's of the layouts to FanView and it will handle the animating.

You even define what elements will trigger the navigation to pop up. A simple call to FanView.showMenu() will toggle the display to pop up or close.

Simple Example
=============================
```java
public class SampleActivity extends Activity {
  /** Called when the activity is first created. */
	private FanView fan;
	
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.test);
        fan = (FanView) findViewById(R.id.fan_view);
        fan.setViews(R.layout.main, R.layout.fan);
    }
    
    public void unclick(View v) {
    	System.out.println("CLOSE");
    	fan.showMenu();
    }
    
    public void click(View v) {
    	System.out.println("OPEN");
    	fan.showMenu();
    }
    
}
````

License
=============================
Copyright 2012 Greg Billetdeaux

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
