# RecyclerView

## [RecyclerView for displaying lists of data](https://developer.android.com/guide/topics/ui/layout/recyclerview#java)


- With RecyclerView -> it's easy to efficiently display large sets of data. 

`Note: Besides being the name of the class, RecyclerView is also the name of the library.`

### Key classes

- `RecyclerView` is the ViewGroup that contains the views corresponding to your data.


- Each individual element in the list is defined by a view holder object.
 After the view holder is created, the RecyclerView binds it to its data. 
 You define the view holder by extending `RecyclerView.ViewHolder.`

- The `RecyclerView` requests those views, by calling methods in the adapter. 
You define the adapter by extending `RecyclerView.Adapter.`

- The layout manager arranges the individual elements in your list. 


### Plan your layout
- RecyclerView items are arranged by a LayoutManager class.
-  **The RecyclerView library provides three layout managers:** 

1. **LinearLayoutManager** -> arranges the items in a one-dimensional list.
2. **GridLayoutManager** arranges all items in a two-dimensional grid:
vertically or horizontally.
3. **StaggeredGridLayoutManager** is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids). 

### Implementing your adapter and view holder

>After implementing layout, you need to implement your Adapter and ViewHolder. 
 The ViewHolder is a wrapper around a View that contains the layout for an individual item in the list. 
 The Adapter creates ViewHolder objects as needed, and also sets the data for those views.
 **binding** is :The process of associating views to their data.

**When you define your adapter, you need to override three key methods:**
1. **onCreateViewHolder():** RecyclerView calls this method whenever it needs to create a new ViewHolder. It creates and initializes, but does not fill in the view's contents.
2. **onBindViewHolder():**  The method fetches the appropriate data and uses the data to fill in the view holder's layout.

3. **getItemCount():** RecyclerView calls this method to get the size of the data set. 

### The Example that from the link:
1. **Java Class**

```java
public class CustomAdapter extends RecyclerView.Adapter<CustomAdapter.ViewHolder> {

    private String[] localDataSet;

    /**
     * Provide a reference to the type of views that you are using
     * (custom ViewHolder).
     */
    public static class ViewHolder extends RecyclerView.ViewHolder {
        private final TextView textView;

        public ViewHolder(View view) {
            super(view);
            // Define click listener for the ViewHolder's View

            textView = (TextView) view.findViewById(R.id.textView);
        }

        public TextView getTextView() {
            return textView;
        }
    }

    /**
     * Initialize the dataset of the Adapter.
     *
     * @param dataSet String[] containing the data to populate views to be used
     * by RecyclerView.
     */
    public CustomAdapter(String[] dataSet) {
        localDataSet = dataSet;
    }

    // Create new views (invoked by the layout manager)
    @Override
    public ViewHolder onCreateViewHolder(ViewGroup viewGroup, int viewType) {
        // Create a new view, which defines the UI of the list item
        View view = LayoutInflater.from(viewGroup.getContext())
                .inflate(R.layout.text_row_item, viewGroup, false);

        return new ViewHolder(view);
    }

    // Replace the contents of a view (invoked by the layout manager)
    @Override
    public void onBindViewHolder(ViewHolder viewHolder, final int position) {

        // Get element from your dataset at this position and replace the
        // contents of the view with that element
        viewHolder.getTextView().setText(localDataSet[position]);
    }

    // Return the size of your dataset (invoked by the layout manager)
    @Override
    public int getItemCount() {
        return localDataSet.length;
    }
}
```
2. **text_row_item.xml** file like this:


```java
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="@dimen/list_item_height"
    android:layout_marginLeft="@dimen/margin_medium"
    android:layout_marginRight="@dimen/margin_medium"
    android:gravity="center_vertical">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/element_text"/>
</FrameLayout>
```