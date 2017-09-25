## Bind text to option
```
     <option *ngFor="let method of contactMethods" [value]="method.id">{{method.name}}</option>
```
## Bind object to option
```
     <option *ngFor="let method of contactMethods" [ngValue]="method.id">{{method.name}}</option>
```

## Multiple selection
```
  <select multiple >
```