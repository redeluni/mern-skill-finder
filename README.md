http://localhost:5000

root: /api/auth

|method|route/api|access|webpage|action  |
|------|---------|------|-------|--------|
|GET   |/auth    |public|.*     |loadUser|
|POST  |/auth    |public|/login |login   |

note:
- completo

---

root: /api/logs
|method|route/api|access |webpage  |action |
|------|---------|-------|---------|-------|
|GET   |/logs    |public |/logs    |getLogs|
|GET   |/logs/:id|public |/logs/:id|getLog |
|POST  |/logs    |private|not used |addLog |
note:
- completo
- da controllare access per tutte e tre le rotte

---
root: /api/posts
|method|route/api                         |access |webpage|action       |
|------|----------------------------------|-------|-------|-------------|
|GET   |/posts                            |private|?      |getPosts     |
|GET   |/posts/:id                        |private|?      |getPost      |
|POST  |/posts                            |private|?      |addPost      |
|DELETE|/posts/:id                        |private|?      |deletePost   |
|POST  |/posts/comment/:id                |private|?      |addComment   |
|DELETE|/api/posts/comment/:id/:comment_id|private|?      |deleteComment|
|PUT   |/posts/like/:id 		          |private|?      |addLike      |
|PUT   |/posts/unlike/:id                 |provate|?      |removeLike   |

note:

---
root: /api/profile
|method|route/api                |access |webpage                       |action           |
|------|-------------------------|-------|------------------------------|-----------------|
|GET   |/profile                 |public |/profiles                     |getProfiles      |
|GET   |/profile/user/:user_id   |public |/profile/:id                  |getProfileById   |
|GET   |/profile/me              |private|/dashboard                    |getCurrentProfile|
|POST  |/profile                 |private|/create-profile, /edit-profile|createProfile    |
|DELETE|/profile                 |private|/dashboard                    |deleteAccount    |
|PUT   |/profile/experience      |private|/add-experience               |addExperience    |
|PUT   |/profile/experience/edit |private|/experience/:id               |editExperience   |
|DELETE|/profile/experience/:id  |private|/experience/:id               |deleteExperience |
|PUT   |/profile/education       |private|/add-education                |addEducation     |
|PUT   |/profile/education/edit  |private|/education/:id                |editEducation    |
|DELETE|/profile/education/:id   |private|/education/:id                |deleteEducation  |
|GET   |/profile/github/:username|public |/profile/:id                  |getGithubRepos   |
|PUT   |/profile/favorite/:id    |private|/profile/:id                  |setFavorite      |
|PUT   |/profile/interviewed/:id |private|/profile/:id                  |setInterviewed   |
|PUT   |/profile/stars/:id       |private|/profile/:id                  |setStars         |
|PUT   |/profile/worked/:id      |private|/profile/:id                  |setWorked        |
|PUT   |/profile/note/:id        |private|/profile/:id                  |saveNote         |


note:
- deleteAccount dovrebbe essere eseguito sulle rotte /api/users
- il codice inerente la modifica e la cancellazione dell'educazione non è stato ancora fatto
-

---
root: /api/users

|method|route/api|access|webpage  |action  |
|------|---------|------|---------|--------|
|POST  |/users   |public|/register|register|

note:
- completo
---