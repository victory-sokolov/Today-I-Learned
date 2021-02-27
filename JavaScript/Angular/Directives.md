# Angular Directives

### ngClass

Helps to use multiple classes

Example 1:

```javascript
<div 
  [ngClass]="['active', 'open']">
</div>
```

Example 2:

if `canAddClass` is `true` we will add `cls-two` class

```javascript
 <div class="cls-one" [ngClass]="{ 'cls-two' : canAddClass }">
	....
</div>
```
