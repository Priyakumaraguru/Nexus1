@Library('shlib1')_
pipeline{
  agent any
  stages{
      stage('Create_Proj')
            {
                steps
                 { 
                    Ncreate_repo(jsondata)
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
                    Ncreate_user(jsondata)
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
                    Nchange_pwd(jsondata)
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
                    Ndown_artifact(jsondata)
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
                    Npart_repo(jsondata)
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
                    Nlist_repos(jsondata)
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
                    Nuserid_info(jsondata)
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
                    Nrepo_status(jsondata)
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
                    NPrivilage(jsondata)
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
         /* stage('Delete_Proj')
            {
                steps
                 { 
                    Ndelete_repo(jsondata)
                    NlogNexus("repo deleted")
    }
    post
    {
    failure
    {
      NlogNexus("repo not deleted")
    }
                 }
            }   */      
            
            
  }
}
