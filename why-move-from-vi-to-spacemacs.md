# Thoughts on moving from Vim to Spacemacs

Do you think it's worth for a beginner developer who still doesn't know much about the big frameworks to spend time learning Emacs?

Especially if said developer has been using Emacs' fabled competitor for over four years now? :sweat_smile:

I was searching for what the best free IDE is, and ended up finding your answer in quora about emacs
https://www.quora.com/What-is-the-best-free-IDE/answer/John-Stevenson-12

Ever since I did a few projects in Racket I have been interested in the lisp scheme syntax, and been dancing with the idea of learning Emacs. But since I found my first job, I've been jumping from (the introduction) of one technology or another because I needed them for my role. Now I'm about to be furloughed, and the dance of learning Emacs seems much more attractive, but I don't know if it's the right time for this.So I'd really appreciate to hear your take on this dilemma. :)

Short answer:  Yes, definitely learn Emacs, start with Spacemacs develop branch and read my book https://practical.li/spacemacs/

> 말로만 듣던 이맥스를 배워야 하나? 이런 고민이 들면, 고민하지 말고 일단 시작하라. 시작은 멀리 가지 말고 스페이스맥스로 하면 된다.

Longer answer:
It sounds like you have the agony of choice, which is a very real problem in our modern world.  There are so many things you can do with your time.  I can offer my experiences as a guide, but only you know how best to spend your time :slightly_smiling_face:

I would certainly recommend looking at Emacs and specifically Spacemacs if you have the time.  There are lots of features you can just drop into Emacs that can help with a wide range of languages.  Arguably Emacs has the most up to date support for the vast majority of languages (with LSP there is even excellent support for Java).

Using a community configuration like Spacemacs means standing on the shoulders of giants, using the cumulative experience of the community to do much more.  So the learning curve for Emacs can be very shallow.

I assume you refer to Vi/Vim as the alternative to Emacs.  I find the Vi style editing (multi-modal) to be amazingly productive and feel lost without it. Ironically, I only learnt Vi style editing when I started using Spacemacs.

I suggest reasons to move away from a specific Vim tool and to Emacs are

1) VimScript (some people find this less than productive) and Emacs lisp is a very effective and elegant programming language with which to configure your editor.

2) Arguably there are more features / better language support generally available in Emacs than Vim

The single biggest change in moving from Vim to Emacs is that you run Emacs once and keep it open all the time.  If you keep closing and opening Emacs, as is often the case with vim, its likely you will find Emacs slow and will be less likely to want to use Emacs instead of Vim.  You can set up a persistent server or daemon process for Emacs too, then use emacsclient command.

If you use a community configuration for Emacs (Spacemacs, Prelude, Doom) then this can save a lot of time setting up the basics.  Using Spacemacs I have discovered lots of very useful features that speed up my work that would have taken a lot longer to discover and configure on my own.

Spacemacs has become my config of choice, so much so I wrote (am still writing) a book on using this.  Initially for Clojure development, but has broadened to a more general Spacemacs / Emacs guide.
https://practical.li/spacemacs/

If you do try Spacemacs, I highly recommend using the develop branch.  It is quite stable and has all the latest bug fixes and new features like Language Server Protocol which many languages are adopting (Clojure already has CIDER which already does a lot more than LSP).

> 스페이스맥스로 VI 에디팅을 배웠다. 말할 것도 없이 이맥스는 VI에 비해 강력하다. 스페이스맥스는 상당히 안정화가 되었고, 이미 저자도 오랜 기간 개바도 하고 글도 쓰는 등 많은 작업을 해오며 검증을 했다. 이맥스는 플랫폼으로써 편집기(?) 안에서 모든 작업을 진행할 수 있다. 수시로 켰다 껏다 할 필요가 없으며 그러면 안된다 (로딩 시간). 더 빠른 로딩을 위해서는 클라이언트 모드로 띄우는 것도 좋은 방법이 될 것이다.
> 또한, 저자는 이맥스+스페이스맥스 위에서 클로져 개발에 필요한 모든 설정을 통합하여 공개했다. 공개만 한 것이 아니라 이렇게 문서도 남겨주었으며 계속 업데이트를 해주고 있다. 이맥스에 대한 구식 자료가 얼마나 많은가? 클로져 개발하려고 하는데 2010년 자료를 볼수는 없지 않은가?
> 나는 VI도 안쓰려고 GUI IDE를 오랫동안 끄적거려 왔다. VSCODE에 상당히 만족하고 쓰고 있었으나, 클로져 개발에는 부족하다는 생각이 들었다. 특히 디버깅 부분이 그렇다. 인텔리제이를 익혀보려고도 했으나 그냥 이맥스 한번 보자라는 생각으로 본 글을 읽어 보았다. 사실 스페이스맥스가 뭔지도 몰랐다.
> 저자는 고수로서 굳이 스페이스맥스를 쓸 필요가 없지 않나 싶다. 배우는 과정에서 자료를 보다보니 이맥스 고수들은 자신의 설정 파일을 떡하기 올려놓고 커스터마이징을 멋지게 해서 쓰고 있지 않은가? 그냥 가져다가 쓰기도 만만치 않다. 설정 파일이 `LISP` 아닌가?!! 근데 이 자료는 스페이스맥스를 쓴다. 뭐야 VI랑 다를게 없네?! 여태 왜 몰랐지 싶을 정도다. 고수들은 더 최적화된 키 입력을 위해서 고민을 많이 한다. 초보자는 흉내내다 보면 포기하게 된다. 이렇게 쉽고 친절한 접근법은 아마 없을 것이다.
> 나 또한 익숙해 지면 뭔가 튜닝을 많이 하려고 들겠지만, 그것은 `나만의 설정`으로 남겨두고 최대한 많은 입문자들이 경험하고 배울 수 있도록 기록을 남겨야 한다. 이 글을 번역할 생각도 없고 그럴 실력도 안된다. 일단 여기서 나오는 주제들을 정리하면서 국내에서 클로져를 입문하는 개발자를 위한 가이드를 만들고 싶다.
