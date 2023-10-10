This is a continuation from your OneNote
## Some Sort of Clean Architecture example involving Interactors and Presentors
```
public class UseCaseInteractor {
  //PresenterClass pres;

  PresenterInterface presenter;

  public UseCaseInteractor(PresenterInterface pres){
    presenter = pres //alias
  }
}
```
Note the PresenterClass implements an _output boundary_, and then then the use case interactor will call methods in the presentor.
```
// In Main.java

PresenterInterface pres = new PresenterClass();
UseCaseInteractor uci = new UseCaseInteractor(pres);
```
