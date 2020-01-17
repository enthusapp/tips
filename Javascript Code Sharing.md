### Mono-repo, Lerna
F/W 에서 Mono-repo 는 흔하다.
F/W 의 어플리케이션 영역이 보통 library 영역보다 작기 때문으로 보인다.

Linux kernel 도 같은 이유로 비슷하다.
git branch 는 Lerna 만큼은 아니지만 비슷한 기능을 제공한다.

### NPM packaging
대부분의 javascript 코드를 공유할때는 편리하다.
하지만 UI, 특히 React Component 를 공유해서 사용할때는 불편한 점도 있다.
Hot Module Replacement 가 npm package update 되어야 할때는 꺼져야 하기 때문이다.

npm package 화 되어있는 React Component 와 프로젝트 코드 둘 다를 동시에 발전시켜야 할때,
매번 npm package 를 업데이트하는 것은 크게 번거로운 작업이다.

다만,
npm package 화 되어있는 React Component 가 타팀 부서원이 담당하거나,
변경의 가능성이 낮고 안정화가 되어있는 완성된 Component 일때,
Component 의 기능이 프로젝트보다 중요하고 공개를 목적으로 작성할때, 등의 상황에서는
npm package 로 되어있는 것이 편리하다.

### Git submodule
npm package 처럼 webpack build 가 필요없다.
version 관리가 package.js 없이 command line interface 만을 사용하기 때문에
더 간단하고 빠르다.

Hot Module Replacement 개발과,
submodule 의 repository 에 바로 commit push 가 가능하다.

하지만,
Component 의 pacakge 의존성 처리를 지원하지 않으며,
사용자의 관리가 제대로 되지 않을 경우 submodule 과 프로젝트 사이의 결합도가 크게 증가할 수 도 있다.

### 결론
정답은 없다.
프로젝트 개발 환경과 성격에 따라 어떤 방식이 유리한지를 고려하여 선택해야 한다.
