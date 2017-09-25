## Create Form
app.module.ts
```
import { FormsModule, ReactiveFormsModule } from '@angular/forms';

imports: [
  FormsModule,
  ReactiveFormsModule
],
```
## Add Validator
Class
```
```

Template
```
import { FormGroup, FormControl, Validators } from "@angular/forms";

@Component({
  selector: "signup-form",
  templateUrl: "./signup-form.component.html",
  styleUrls: ["./signup-form.component.css"]
})
export class SignupFormComponent implements OnInit {
  form = new FormGroup({
    username: new FormControl('', Validators.required),
    password: new FormControl()
  });
}
```