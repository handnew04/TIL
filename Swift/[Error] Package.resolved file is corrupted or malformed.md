1. 파인더 해당 프로젝트 폴더
2. 앱이름.xcodeproj 파일 우클릭 → 패키지 내용 보기
3. project.xcworkspace 우클릭 → 패키지 내용 보기
4. xcshareddata → swiftpm → Package.resolved 파일 삭제
5. 프로젝트 재실행
6. File → Packages → Reset Packages Cashes

해당 파일은 SPM을 사용시 Xcode가 만드는 파일인데, 해당 프로젝트를 작업하는 모든 개발자는 같은 버전의 의존성 패키지를 사용해야한다.
