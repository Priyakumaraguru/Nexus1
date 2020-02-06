@Library('shlib1')_
pipeline{
  agent any
  stages{
      stage('Create_Proj')
            {
                steps
                 { 
                    Ncreate_repo(jsondata)
                    
                 }
            }
      stage('part_details')
            {
                steps
                 { 
                    Npart_repo(jsondata)
                    
                 }
            }  
      stage('Repo_details')
            {
                steps
                 { 
                    Nlist_repos(jsondata)
                    
                 }
            }
      stage('Down_arti')
            {
                steps
                 { 
                    Ndown_artifact(jsondata)
                    
                 }
            }
       stage('Delete_Proj')
            {
                steps
                 { 
                    Ndelete_repo(jsondata)
                    
                 }
            }
            
        stage('Create_user')
            {
                steps
                 { 
                    Ncreate_user(jsondata)
                    
                 }
            }
         stage('User_info')
            {
                steps
                 { 
                    Nuserid_info(jsondata)
                    
                 }
            }
         stage('repo_status')
            {
                steps
                 { 
                    Nrepo_status(jsondata)
                    
                 }
            }
          stage('userpassword_change')
            {
                steps
                 { 
                    Nchange_pwd(jsondata)
                    
                 }
            }
          stage('Artifact_down')
            {
                steps
                 { 
                    Ndown_artifact(jsondata)
                    
                 }
            }       
         stage('privilege')
            {
                steps
                 { 
                    NPrivilage(jsondata)
                    
                 }
            }
                    
            
            
  }
}
