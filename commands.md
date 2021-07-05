

fastapi uvicorn sqlalchemy graphene graphene-sqlalchemy alembic psycopg2 black python-dotenv

alembic init alembic

docker-compose run app alembic revision --autogenerate -m "New Migration" 
docker-compose run app alembic upgrade head

mutation CreateNewPost{
  createNewPost(title:"new title1", content:"new content") {
    ok
  }
}

query{
  allPosts{
    title
  }
}

query{
  postById(postId:2){
    id
  	title
    content
  }
}