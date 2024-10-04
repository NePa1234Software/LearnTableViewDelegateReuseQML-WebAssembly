# LearnTableViewDelegateReuseQML-WebAssembly

This is a small project for learning and teaching QML TableView delegate pooling and delegate reuse.

For more details, read here: https://doc.qt.io/qt-6/qml-qtquick-tableview.html#reusing-items

The demo shows 
- the difference when using the TableView.reuseItems property 
- how the delegate objects are created, pooled and reused
- different method of destroying the delagate (each has its drawbacks)


The main takeaway here is the fact that a delegate IS still alive even if not enabled, not visible or is pooled.
This can become important if the delegate consumes a lot of resourses, e.g. uses heavy graphics or even streaming services etc.

Delegate reuse just parks the delegate until scrolled into view again. The table roles are switched to the new values but the object is the same. This is an enormous performance boost compared to creating and destroying the QML objects over and over again. the object name in the top left corner of each table cell demonstrates this. The color animation is there to show that I have also stopped all animation once the delegate is switched to "pooled" state. 

Normally clipping is used such that the table cells are not visible outside the table border, but keeping it visible (unclipped) in this demo shows also exactly when and IF the delegates are sent to the pool. 

This demo shows how to use the TableView.pooled and TableView.reused signal, of coarse there are equivalents for ListView etc. 

See the details in the provided tooltips.

## Live Online

URL: https://nepa1234software.github.io/LearnTableViewDelegateReuseQML-WebAssembly/appLearnTableViewPoolDemoQML.html

## Code

Repo URL: https://github.com/NePa1234Software/LearnTableViewDelegateReuseQML

## Licensing

See the license file and License Folder for details
- The program is build using the Qt Framework opensource version (https://www.qt.io/licensing/)
- WebAssembly build powered by emscription SDK (https://emscripten.org/docs/introducing_emscripten/emscripten_license.html)

