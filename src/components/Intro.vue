<script setup>
import {introText} from "../constants"
</script>
<template>
    <section id="intro">
        <div class="intro__inner">
            <h2 class="intro__title">
               {{introText.title}}
            </h2>
            <div class="intro__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="intro__text">
                <div class="text">
                    <div>{{ introText.desc[0]}}</div>
                </div>
                <div className="img">
                    <img src="@/assets/img/about.jpg" alt="어바웃" />
                </div>
                <div className="mini__image">
                    <div className="img1">
                        <p>REACT.JS</p>
                    </div>
                    <div className="img2">
                        <p>JAVA SCRIPT</p>
                    </div>
                
                   
                    <div className="img3">
                        <p>NODE.JS </p>
                    </div>
                </div>
                <div className="mini__image2">
                    <div className="img1">
                        <p>HTML<br/>&CSS</p>
                    </div>
                    <div className="img2">
                        <p>SQL</p>
                    </div>
                
                   
                    <div className="img3">
                        <p>TYPE SCRIPT </p>
                    </div>
                </div>

            </div>
            <div class="intro__lines bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
  #intro {
    height: 100vh; //화면을 100등분해서 채웠다는 의미
}

.intro__inner {
    width: 100%;
    height: 100%;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column; //줄바꿈을 해주어 선이 글씨 밑으로 나오게 하기 위함
    padding: 16px;
    margin-top: 60px;
   

    @media (max-width: 800px){
        justify-content: center;// pc화면에서는 내려가 있다가 핸폰 화면에서는 중앙에 위치

    }
    
    .intro__title {
        font-size: 9.7vw;
        text-transform: uppercase;
        line-height: 1.8;
        font-weight: 800;
        white-space: nowrap;//글씨 한줄 만들기
        text-indent: -0.5vw; //글씨 들여쓰기
        letter-spacing: -0.3vw;
        color:#fff;

        @media(max-width: 1500px){
            font-size: 9.3vw;
        }

        @media(max-width: 600px){
            font-size: 8vw;
        }

        @media(max-width: 320px){
            display: none;
        }
    }
    .intro__text {
        width: 100%;
        height: 40vh;
        background-color: #0a1533;
        color: var(--white);
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        position: relative;

        .text{
            font-size: 3vw;
            line-height: 1;
            font-weight: 900;
            text-transform: uppercase;
            text-decoration: underline;
            text-align: center;
            position: relative;
            z-index: 100;
            transition: all 0.3s;
            cursor: all-scroll;
            margin-left: 150px;
            
    
            @media(max-width: 1300px){
                font-size: 40px;
            }
            @media(max-width: 600px){
                left:5%;
            }
            @media(max-width: 750px){
                font-size: 30px;
            }
            @media(max-width: 600px){
                left:5%;
            }
            @media(max-width: 550px){
                    display: none;
            }
        }

        
        .img {
            position: absolute;
            left: 20%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 30vh;
            height: 30vh;
            border-radius: 50%;
            overflow: hidden;
            filter: grayscale(100%);//완전히 흑백으로 처리하게 하는 것이다.
            transition: all 0.3s;

            @media(max-width: 1000px){
                width: 20vh;
                height: 20vh;
            }

            @media(max-width: 550px){
                width: 25vh;
                height: 25vh;
                left: 50%;
            }

            @media(max-width: 350px){
                width: 15vh;
                height: 15vh;
                left: 50%;
            }
          
          

        }
        .mini__image {
                display: inline-block;

                .img1{    
                    position: absolute;
                    left: 50%;
                    top: 24%;
                    transform: translate(-40%, 0%);
                    width: 18vh;
                    height: 16vh;
                    overflow: hidden;
                    transition: all 0.3s;
                    opacity: 0;
                   

                  p {
                    font-size: 1.5rem;
                

                    @media(max-width: 900px){
                        font-size: 1rem;
                    }  
                  }

                  @media(max-width: 900px){
                    width: 13vh;
                    height: 13vh;
                    
    
                }  

                }

                @media(max-width: 550px){
                        display: none;
                 }
            
                 .img2{    
                    position: absolute;
                    left: 70%;
                    top: 18%;
                    transform: translate(-40%, 0%);
                    width: 18vh;
                    height: 16vh;
                    overflow: hidden;
                    transition: all 0.3s;
                    opacity: 0;
                   

                  p {
                    font-size: 1.5rem;

                    @media(max-width: 900px){
                        font-size: 1rem;
                    }  
                  }

                  @media(max-width: 900px){
                    width: 13vh;
                    height: 13vh;
                    top: 24%;
                  }  

                

                }

                @media(max-width: 550px){
                        display: none;
                        .img2{    
                            position: absolute;
                            top: 26%;
                        }
                 }

                 .img3{    
                    position: absolute;
                    left: 90%;
                    top:  24%;
                    transform: translate(-40%, 0%);
                    width: 18vh;
                    height: 16vh;
                    overflow: hidden;
                    transition: all 0.3s;
                    opacity: 0;
                   

                  p {
                    font-size: 1.5rem;

                    @media(max-width: 900px){
                        font-size: 1rem;
                    }  
                  }

                  @media(max-width: 900px){
                    width: 13vh;
                    height: 13vh;
                    
    
                }  

                }

                @media(max-width: 550px){
                        display: none;
                 }
        }

        .mini__image2 {
            display: inline-block;

            .img1{    
                position: absolute;
                left: 50%;
                top: 60%;
                transform: translate(-40%, 0%);
                width: 18vh;
                height: 16vh;
                overflow: hidden;
                transition: all 0.3s;
                opacity: 0;
               

              p {
                font-size: 1.5rem;

                @media(max-width: 900px){
                    font-size: 1rem;
                }  
              }

              @media(max-width: 900px){
                width: 13vh;
                height: 13vh;
                

            }  

            }

            @media(max-width: 550px){
                    display: none;
             }
        
             .img2{    
                position: absolute;
                left: 70%;
                top: 60%;
                transform: translate(-40%, 0%);
                width: 18vh;
                height: 16vh;
                overflow: hidden;
                transition: all 0.3s;
                opacity: 0;
               

              p {
                font-size: 1.5rem;

                @media(max-width: 900px){
                    font-size: 1rem;
                }  
              }

              @media(max-width: 900px){
                width: 13vh;
                height: 13vh;
                margin-left: 3vh;
            }  

            }

            @media(max-width: 550px){
                    display: none;
                    .img2{    
                        position: absolute;
                        top: 26%;
                    }
             }

             .img3{    
                position: absolute;
                left: 90%;
                top:  60%;
                transform: translate(-40%, 0%);
                width: 18vh;
                height: 16vh;
                overflow: hidden;
                transition: all 0.3s;
                opacity: 0;
               

              p {
                font-size: 1.5rem;

                @media(max-width: 900px){
                    font-size: 1rem;
                    margin-right: 5vh;
                }  
              }

              @media(max-width: 900px){
                width: 13vh;
                height: 13vh;
                

            }  

            }

            @media(max-width: 550px){
                    display: none;
             }
    }



        
        
        &:hover .text {
            opacity: 0;
        }
        &:hover .text2, &:hover .img1, &:hover .img2, &:hover .img3 
        , &:hover .img4, &:hover .img5, &:hover .img6{
            opacity: 1;
        }

        &:hover .img {
            filter: grayscale(0);
        }
    }
    .intro__lines {
       width: 100%;
       

       .line {
            display: block;
            width: 100%;
            height: 1px;
            background-color: #0a1533;
            margin-bottom: 0.5vw;

            &:nth-child(1) {
                height: 1px;
            }
            &:nth-child(2) {
                height: 2px;
            }
            &:nth-child(3) {
                height: 5px;
            }
            &:nth-child(4) {
                height: 9px;
            }
            &:nth-child(5) {
                height: 9px;
            }
            &:nth-child(6) {
                height: 12px;
            }

            &:nth-child(7) {
                height: 25px;
            }
        }

        &.bottom {
           .line { 
                margin-top: 0.5vw;
                margin-bottom: 0;
                display: none;
                color: #0a1533;

                @media (max-width: 1000px){
                    display: block;
                }

                &:nth-child(1){
                    height: 17px;
                }
                &:nth-child(2){
                    height: 15px;
                }
                &:nth-child(3){
                    height: 11px;
                }
                &:nth-child(4){
                    height: 9px;
                }
                &:nth-child(5){
                    height: 5px;
                }
                &:nth-child(6){
                    height: 2px;
                }
                &:nth-child(7){
                    height: 1px;
                }
            }
        }
    }
}
</style>