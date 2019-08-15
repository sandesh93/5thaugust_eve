#!/usr/bin/env groovy
import java.net.URL

node{
    stage('Git Checkout'){
        git 'https://github.com/edureka-git/DevOpsClassCodes.git'
    }
    stage('AB Compile'){
        withMaven(maven:'MyMaven'){
            sh 'mvn compile'
        }
    }
    stage('AB CodeReview'){
        wihMaven(maven:'MyMaven'){
            sh 'mvn pmd:pmd'   
        }
        // publish visuals of target/pmd.xml
    }
    stage('AB Package'){
        withMaven(maven:'MyMaven'){
            sh 'mvn package'
        }
    }
}
