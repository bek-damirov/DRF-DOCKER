# DRF-DOCKER
Django-REST, по созданию постов, комментариев к ним и оценок от 1 до 5 с регистрацией автора и гостя.
Завернут в Docker с базой данных Postgres.

запуск докера;

docker-compose build,

docker-compose up -d,

docker-compose exec db psql --username=test_user --dbname=test_db.

документация:

/redoc
/swagger


api/accounts/register/quest/ только для просмотра,
api/accounts/register/author/- регистрация автора может создавать посты и комментарии,
api/post/create/ - создать пост,
api/post/int(id поста)/ - удаление, изменение поста(только автором),
'api/comments/'-просмотр всех комментариев,
'api/post/<int:post_id>/comment/ - комментарий к посту,
'api/comment/<int:pk>/ - удаление, изменение комментария(автором),
'api/post/status/' - просмотр оценок,
'api/post/<int:post_id>/status/' - оценка к постам,
'api/status/<int:pk>/' - удаление, изменение оценки(автором),
'api/comment/status/' - просмотр оценок к комментариям,
'api/comment/<int:comment_id>/status/' - оценка к комментариям,
'api/status/<int:pk>/' - удаление изменения оценок,
 
