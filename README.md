# LearnTableViewDelegateReuseQML-WebAssembly

This is a small project for learning and teaching QML TableView delegate pooling and delegate reuse.

The demo shows 
- the difference when using the TableView.reuseItems property 
- how the delegate objects are created, pooled and reused
- different method of destroying the delagate (each has its drawbacks)


The main takeaway here is the a delegate IS still alive even if not enabled, not visible or is pooled.
This can become important if the delegate consume a lot of resourses, use heavy graphics or even streaming services etc.

Delegate reuse just parks are delegate until scrolled into view again. The table roles are switched to the new values but the object is the same. This is an enormous performance boost compared to creating and destroying the QML objects over and over again.

See the details in the provided tooltips.

## Live Online

URL: https://nepa1234software.github.io/LearnTableViewDelegateReuseQML-WebAssembly/appLearnTableViewDelegateReuseQML.html

## Codeor te

Repo URL: https://github.com/NePa1234Software/LearnTableViewDelegateReuseQML

## Licensing

See the license file and License Folder for details
- The program is build using the Qt Framework opensource version (https://www.qt.io/licensing/)
- WebAssembly build powered by emscription SDK (https://emscripten.org/docs/introducing_emscripten/emscripten_license.html)

