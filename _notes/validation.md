## FormControl
  Each of the input field in the form need a FormControl
  - value
  - touched     : received focus
  - untouched
  - dirty       : value is changed
  - pristine    : value is not changed
  - valid
  - errors

## FormGroup
  - value
  - touched
  - untouched
  - dirty : value is changed
  - pristine : means the value is not changed
  - valid
  - errors

## Validation
```
<input required minlength="3" maxlength="10" pattern="" ngModel name="firstName" #firstName="ngModel" (change)="log(firstName)" id="firstName" type="text" class="form-control" />
    <div class="alert alert-danger" *ngIf="firstName.touched && !firstName.valid">
      <div *ngIf="firstName.errors.required"> First Name is required.</div>
      <div *ngIf="firstName.errors.minlength"> First Name should be mininum {{firstName.errors.minlength}} characters.</div>
      <div *ngIf="firstName.errors.pattern"> First Name doesn't match the pattern.</div>
    </div>
```
Use log(firstName) to show all properties on formControl

## Validation style
  Find it in Chrome 
```
.form-control.ng-touched.ng-invalid{
  border:12px solid red; 
}
```

## Disable button
```
<form #f="ngForm" (ngSubmit)="submit(f)">
  <button class="btn btn-primary" [disable]="!f.valid">Submit</button>
</form>
```

## Diagnostic tool
```
<p>
  {{f.value| json}}
</p>

```