```
<div *ngFor="let method of contactMethods "class="radio">
  <label for="">
    <input type="radio" name="contactMethod" [value]="method.id">{{method.name}}
  </label>
</div>
```