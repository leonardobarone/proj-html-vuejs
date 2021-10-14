<template>
    <div id="learn">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-12 col-md-5 col-left">
                    <div class="col-12 title">
                        <p>WHY HESITATE TO REGISTER?</p>
                        <h3>Learn At Your Own <span>Pace</span></h3>
                        <ul class="list-learn">
                            <li><i class="fas fa-check"></i> Select & customize courses to your preferences</li>
                            <li><i class="fas fa-check"></i> Change the tutor and make arrangements</li>
                            <li><i class="fas fa-check"></i> Participate in events to join others</li>
                            <li><i class="fas fa-check"></i> Get the desired certificate delivered at house</li>
                        </ul>
                        <div class="bottone">
                            <a href="#" class="btn btn-1">Get started for free</a>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-7 col-right">
                    <div class="container-img-1">
                        <img width="100%" class="learn-1" src="../assets/materiale/images/learn-1.png" alt="">
                    </div>
                </div>
            </div>
            <div class="row align-items-center">
                <div class="col-12 col-md-7 col-left-2">
                   <div class="container-img-2">
                        <img width="100%" class="learn-2" src="../assets/materiale/images/learn-2.png" alt="">
                    </div>
                </div>
                <div class="col-12 col-md-5 col-right-2">
                     <div class="col-12 title">
                        <p>WHY HESITATE TO REGISTER?</p>
                        <h3>Learn At Your Own <span>Pace</span></h3>
                        <div class="text">Save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activities of enjoyment or other precious moments.</div>
                        <div class="bottone">
                            <a href="#" class="btn btn-1">Download Our App</a>
                        </div>
                     </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Learn",
}
</script>

<style scoped lang="scss">
@import '../assets/style/common.scss';
@media screen and (max-width: 48rem){
    .container-img-1::after,
    .container-img-2:before,
    .col-left-2 {
    display: none;
    }
    #learn .row:first-child {
        margin-bottom: 3.125rem !important;
    }
    .title {
        p {
            text-align: center;
        }
        h3 {
            text-align: center;
            width: 100%;
        }
    }
    .bottone {
        text-align: center;
    }
}
#learn {
    .row:first-child {
        margin-bottom: 4.6875rem;
    }
    padding: 3.125rem 0rem;
    .title {
        p {
          @include p-top-title;
        }
        h3 {
          @include title-intro;
          margin-bottom: .625rem;
          span {
            @include span-title-intro;
          }
        }
        .list-learn {
            padding: .9375rem;
            font-size: .875rem;
            li {
                margin-bottom: .3125rem;
                i {
                    color: var(--threeColor);
                    margin-right: .625rem;
                }
            }
        }
    }
}

.col-right {
    .learn-1 {
        display: block;
    }
    .container-img-1 {
        position: relative;
        padding: 2.5rem;
    }
    .container-img-1::before {
        content: "";
        background-image: url("../assets/materiale/underlay-shape-grey.svg");
        background-repeat: no-repeat;
        background-position: left bottom;
        background-size: 70%;
        z-index: -10;
        position: absolute;
        top: 0;
        left: .625rem;
        bottom: 0rem;
        right: 0;
    }
    .container-img-1::after {
        content: "";
        background-image: url("../assets/materiale/images/circle-points.png");
        background-repeat: no-repeat;
        background-size: contain;
        height: 9.375rem;
        width: 9.375rem;
        position: absolute;
        top: calc(70% - 4.6875rem);
        right: 1.25rem;
        z-index: -20;
    }
}
.text {
    margin-bottom: .9375rem;
    padding: .625rem;
}

.col-left-2 {
    .learn-2 {
        display: block;
        margin: 0 auto;
        width: 80%;
    }
    .container-img-2 {
        position: relative;
    }
    .container-img-2:after {
        content: "";
        background-image: url("../assets/materiale/underlay-shape-grey.svg");
        background-repeat: no-repeat;
        background-size: 70%;
        background-position: left bottom;
        position: absolute;
        z-index: -10;
        top: 0rem;
        left: 0rem;
        bottom: 0rem;
        right: 0rem;
    }

    .container-img-2:before {
        content: "";
        background-image: url("../assets/materiale/images/linee.png");
        background-repeat: no-repeat;
        height: 9.375rem;
        width: 9.375rem;
        background-size: contain;
        background-position: center;
        position: absolute;
        z-index: -10;
        top: 6.25rem;
        left: .625rem;
        bottom: 0rem;
        right: 0rem;
    }
}


</style>