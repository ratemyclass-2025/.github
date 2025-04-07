METHOD PATH                             JSON ATTRIBUTES
POST   /user/                           email, password
GET    /user/   
POST   /user/verify-email               email, token
POST   /user/verify-password            email, newPassword, token
POST   /user/reset-password             email
POST   /user/sessions                   email, password
DELETE /user/{id}    
GET    /user/{id}    
PATCH  /user/{id}                       email?, password?

GET    /statistic/       
GET    /statistic/{id}          
GET    /statistic/discipline/{id}

POST   /discipline/                     code, name, professor, course, center, period, type (MANDATORY, ELECTIVE_PROFILE, ELECTIVE_FREE), hours
GET    /discipline/{id}   
GET    /discipline/        
PUT    /discipline/{id}                 code?, name?, professor?, course?, center?, period?, type? (MANDATORY, ELECTIVE_PROFILE, ELECTIVE_FREE), hours?
DELETE /discipline/{id} 
GET    /discipline/favorite/{id}        id, code?, name?, professor?, course?, center?, period?, type? (MANDATORY, ELECTIVE_PROFILE, ELECTIVE_FREE), hours?, ordem? (asc, desc), ordemBy?

POST   /reaction/                       type, materialId, userId, disciplineId
GET    /reaction/   
DELETE /reaction/{id}   
PATCH  /reaction/{id}                   type?, materialId?, userId?, disciplineId?
GET    /reaction/{id}      

POST   /review/                         disciplineId, userId, finalGrade, professorTeachingScore, periodPaid, droppedOut, passedFirstTry, difficultyLevel, disciplineScore, comment, recommendation
GET    /review/   
DELETE /review/{id}   
PATCH  /review/{id}                     disciplineId?, userId?, finalGrade?, professorTeachingScore?, periodPaid?, droppedOut?, passedFirstTry?, difficultyLevel?, disciplineScore?, comment?, recommendation?
GET    /review/{id}   

POST   /material/                       title, link, userId, disciplineId
GET    /material/                       disciplina?, curso?, professor?, ordem?, ordemBy?
GET    /material/{id}                   disciplina?, curso?, professor?, ordem?, ordemBy?
DELETE /material/{id}   
PATCH  /material/{id}                   title?, link?, userId?, disciplineId?
GET    /material/{id}   
