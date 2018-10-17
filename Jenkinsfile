pipeline{
     agent any
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
                                              branch "master"

                                            }
                                        }
                                    steps{
                                           echo 'fail'
                                         }

                                    }

                stage ('Final'){
                                parallel{
                                         stage('test1'){
                                                       steps{
                                                             echo 'success'
                                                            }
                                                        }
                                         stage('test2'){
                                                       agent{
                                                             docker{
                                                                    reuseNode false
                                                                    image 'ubuntu'
                                                                    }
                                                             }
                                                        }
                                          }
                                 }



                                         
                                                         

                      

                 }


        }

         
