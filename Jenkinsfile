pipeline{
     agent any{
             stages{

                stage ('primary'){
                               steps{
                                      echo 'hi'
                                    }
                                 }

                stage ('secondary'){
                               steps{

                                     input('Do you want to proceed?')

                                    }

                                   }

                stage ('condition'){

                                   when{

                                         not{
                                              branch "maste"

                                            }
                                        }
                                    steps{
                                           echo 'fail'
                                         }

                                    }

                      }

                 }


        }

         
