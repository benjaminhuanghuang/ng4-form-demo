## Create form component
  $ ng g c my-form

## Create input elements in from 
  ```
  div.form-group>label+input[type='text'].form-control

  div.form-group>label[for='comment']+textarea[id='comment'].form-control

  div.form-group>label[for="contactMethod"]+select[id="contactMethod"].form-control
  ```

## Import FormsModule into app.module
```
import { FormsModule } from '@angular/forms';

@NgModule({
  declarations: [
  ],
  imports: [
    BrowserModule, FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```