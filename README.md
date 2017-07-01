Table form
==============
2017-07-01


A simple form markup based on table, to quickly create/style your forms.




[![table-form.png](https://s19.postimg.org/iwvpalotf/table-form.png)](https://postimg.org/image/5sq4xwwrj/)





How to
============

First, include the **table-form** css file in your project.


Then below you'll find the original markup for a popup use case.
Adapt to your needs.



```html
<div class="hidden">
    <div id="write-comment-popup">
        <form action="" method="post" class="table-form">
            <div class="table-form-title">
                <h3>Type in your comment</h3>
            </div>
            <table>
                <tr>
                    <td>
                        <label>Title</label>
                    </td>
                    <td>
                        <input type="text" name="title" value="">
                    </td>
                </tr>
                <tr>
                    <td>
                        <label>Comment</label>
                    </td>
                    <td>
                        <textarea name="comment"></textarea>
                    </td>
                </tr>
                <tr>
                    <td>
                        <label>Rating</label>
                        <span class="hint">(5 is the best)</span>
                    </td>
                    <td>
                        <select name="rating">
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                            <option value="5">5</option>
                        </select>
                    </td>
                </tr>
            </table>
            <div class="table-form-bottom">
                <button class="cancel-btn">Cancel</button>
                <button type="submit" class="submit-btn">Submit</button>
            </div>
        </form>
    </div>
</div>
```


To use the table-form markup, ensure that you do the following:

- .table-form on the form
- .table-form-title h3 if you need a title
- table with only two columns for the main content, no particular markup
- .table-form-bottom with buttons inside for the bottom buttons, you can use two built-in classes:
    - .cancel-btn, create a grayish button 
    - .submit-btn, create a greenish button (of course you can change the color if you want)




How to handle errors?
=======================

In terms of markup, just add another tr with class error below the erroneous tr, like this for instance:


```html
 <!-- ... -->
 <tr>
    <td>
        <label>Title</label>
    </td>
    <td>
        <input type="text" name="title" value="">
    </td>
</tr>
<tr class="error hidden">
    <td></td>
    <td>This field is required</td>
</tr>
<!-- ... -->
```


The OnTheFlyForm planet (see related section) has a js script that helps you with validating your controls.




Related
===========
- https://github.com/lingtalfi/OnTheFlyForm




History Log
------------------ 
    
- 1.0.0 -- 2017-04-04

    - initial commit