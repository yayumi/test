# git_command

// git status -> git commit -a -> git push
// git pull -> git status -> git commit -> git push

# commit 히스토리 확인
git log --graph 

# 강제 push
git push origin <repo_name> --force 

# 파일 실행 권한 주기
git update-index --chmod=+x autogen.sh #파일 실행 권한 주기

1. 작업의 취소

git reset --soft HEAD^
--soft 옵션을 사용하였으므로, 수정한 내역은 그대로 두고 head는 한단계 위로 조정을 한다는 의미입니다. commit을 취소하는 것이죠
--hard 옵션을 사용하게 되면 지금까지 작업하던것들이 다 날아가므로, 조심합시다

2. commit의 취소

git reset --hard @^
hard를 이용하여 HEAD로 돌리는 명령어 입니다.
@는 1.8.4부터 도입된 HEAD의 동의어라고 합니다. 같은걸로는 @^, @~1, @~ 가 동일합니다.

3. pull, merge 취소

git reset --hard ORIG_HEAD
git reset --merge ORIG_HEAD