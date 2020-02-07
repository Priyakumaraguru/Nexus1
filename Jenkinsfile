@Library('shlib1')_
pipeline{
  agent any
  stages{
      stage('Create_Proj')
            {
                steps
                 { 
                    Ncreate_repo(JSON)
                   NlogNexus("Repo is created")
    }
    post
    {
    failure
    {
      NlogNexus("Repo not created")
    }
    
                 }
            }
     stage('Create_user')
            {
                steps
                 { 
                    Ncreate_user(JSON)
                    NlogNexus("User is created")
    }
    post
    {
    failure
    {
      NlogNexus("User not created")
    }
                 }
            }
    stage('userpassword_change')
            {
                steps
                 { 
                    Nchange_pwd(JSON)
                     NlogNexus("User password is changed")
    }
    post
    {
    failure
    {
      NlogNexus("User password is not changed")
    }
                 }
            }
    stage('Artifact_down')
            {
                steps
                 { 
                    Ndown_artifact(JSON)
                    NlogNexus("Artifact is downloaded")
    }
    post
    {
    failure
    {
      NlogNexus("Artifact is not downloaded")
    }
                 }
            }  
      stage('part_details')
            {
                steps
                 { 
                    Npart_repo(JSON)
                    NlogNexus("repo details collected")
    }
    post
    {
    failure
    {
      NlogNexus("repo details not collected")
    }
                 }
            }  
    
      stage('Repo_details')
            {
                steps
                 { 
                    Nlist_repos(JSON)
                    NlogNexus("Repository details are collected")
    }
    post
    {
    failure
    {
      NlogNexus("Repository details are not collected")
    }
                 }
            }
      
      
         stage('User_info')
            {
                steps
                 { 
                    Nuserid_info(JSON)
                    NlogNexus("User information is collected")
    }
    post
    {
    failure
    {
      NlogNexus("User information is not collected")
    }
                 }
            }
         stage('repo_status')
            {
                steps
                 { 
                    Nrepo_status(JSON)
                    NlogNexus("repo status collected")
    }
    post
    {
    failure
    {
      NlogNexus("repo status not collected")
    }
                 }
            }
               
         stage('privilege')
            {
                steps
                 { 
                    NPrivilage(JSON)
                    NlogNexus(" security privileges retrived")
    }
    post
    {
    failure
    {
      NlogNexus("security privileges not retrived")
    }
                 }
            }
          stage('Delete_Proj')
            {
                steps
                 { 
                    Ndelete_repo(JSON)
                    NlogNexus("repo deleted")
    }
    post
    {
    failure
    {
      NlogNexus("repo not deleted")
    }
                 }
            }     
            
            
  }
}
