
# ViewControllers in Xib files

(replace `TestViewController` with your desired class name)

## Creating a new ViewController

- Add the new files:
  - New File > `TestViewController`
  - Check the "Also create XIB file"
- Open the Xib file
  - delete the created view
  - clear the File Owner class
  - Drag a ViewController objects and set the class to `TestViewController`
  - With this setup you will have `layoutGuides` / `safeArea` compatible with iOS 9-11

## Instantiating the ViewController

- Instantiate manually:
  `UINib(nibName: "TestViewController", bundle: nil).instantiate(withOwner: nil, options: nil).first as? TestViewController`

- Use a helper library like `R.swift` (it will pick up your Xib name and camelCase it):
  `R.nib.testViewController.firstView(owner: nil)`
