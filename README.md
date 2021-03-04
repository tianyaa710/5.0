# 5.0
软件环境：Apache Tomcat 5.0
void Game::drawThisEnemyToNull( Frame f )

{

drawFrame(f, ' ', ' ');

}

 

void Game::judgeEnemy()

{

for(int i = 0; i < 8; i++)

for(int j = 0; j < 10; j++)

if( judgeCoordInFrame(enemy[i], bullet[j]) )

{

score += 5;

drawThisEnemyToNull( enemy[i] );

COORD a={1, 1};

COORD b={45, 3};

enemy[i].position[0] = random(a, b);

enemy[i].position[1].X = enemy[i].position[0].X + 3;

enemy[i].position[1].Y = enemy[i].position[0].Y + 2;

drawThisBulletToNull( bullet[j] );

bullet[j].Y = 30;

}

}

void Game::Shoot()

{

for(int i=0; i<10; i++)

if(bullet[i].Y == 30)

{

bullet[i].X = position[5].X;

bullet[i].Y = position[5].Y-1;

break;

}
