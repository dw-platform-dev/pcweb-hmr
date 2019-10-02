pcweb-hmr
===================================
[더반찬 PC](www.thebanchan.co.kr)


[The Git Flow](http://cms.esolution.com/?p=1343)
==================

* Create a branch
* Add commits
* Open a Pull Request
* Discuss and Review your code
* Deploy
* Merge


Updating/The Development Cycle
------------

* master, develop 브랜치 두 가지로 분기로 나눕니다.

####절대 ***master*** branch에 직접 커밋하지 않습니다.

####절대 ***develop*** branch에 직접 커밋하지 않습니다.

항상 개발 브랜치에서 시작하시기바랍니다.
	git checkout develop
	git checkout -b feature/{branch}

	git add .
	git commit -am "I have made some changes."

	git checkout develop
	git merge --no-ff feature/{branch}
	git push origin develop


Releasing
------------

- Create a feature branch as normal.
- Update the version history in the README.md file
- Update this to develop as normal.

		git checkout master
		git merge --no-ff develop
		git push origin master
		git tag v1.0.0
		git push origin v1.0.0

Replace 1.0.0 in the snippet here with your appropriate versions. Now you have a tag saved.
