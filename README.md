# TabPages
Small component to enable tabbing pages with Bootstrap 4 cards (or some other paging elements).

Small Demo: http://vandango.org/github/tabPagesDemo/


#### HTML
```html
<div class="card text-center" data-tabs="myTabPage">
  <div class="card-header">
    <ul class="nav nav-tabs card-header-tabs">
      <li class="nav-item"><a class="nav-link" href="#" data-tab-page="page1">Page 1</a></li>
      <li class="nav-item"><a class="nav-link" href="#" data-tab-page="page2">Page 2</a></li>
      <li class="nav-item"><a class="nav-link" href="#" data-tab-page="page3">Page 3</a></li>
    </ul>
  </div>
  <div class="card-block" data-tab-page="page1">
    <h4 class="card-title">Special title treatment 1</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
  <div class="card-block" data-tab-page="page2">
    <h4 class="card-title">Special title treatment 2</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
  <div class="card-block" data-tab-page="page3">
    <h4 class="card-title">Special title treatment 3</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

#### JavaScript Call
```javascript
$(function() {
  // basic initialization, without object possible
  TabPages.init('myTabPage');

  // to pre-select you need the object itself
  var tab = TabPages.init('myTabPage');
  tab.selectTab('page3');
  
  // or do it the classic way
  var myTabElement = new TabPages('myTabPage');
  myTabElement.initTabs();
  myTabElement.selectTab('page3');
});
```
