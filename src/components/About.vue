<template>
    <div>
        <h1>About Me</h1>
        <p>My name is Martin Heinz and I'm a software developer/DevOps engineer. I'm from Slovakia, living in Bratislava and currently working at IBM.
            You can find me on
            <a class="no-underline" href="https://github.com/Panda-ManR" target="_blank">
            <v-hover>
                <font-awesome-icon :icon="['fab', 'github']" @mouseover="next_active = true" @mouseout="next_active = false"
                                   slot-scope="{ hover }"
                                   :class="`${hover? 'icon-active': 'icon-inactive'}`"/>
            </v-hover>
            </a>,
            <a class="no-underline" href="https://www.linkedin.com/in/heinz-martin" target="_blank">
            <v-hover>
                <font-awesome-icon :icon="['fab', 'linkedin']" @mouseover="next_active = true" @mouseout="next_active = false"
                                   slot-scope="{ hover }"
                                   :class="`${hover? 'icon-active': 'icon-inactive'}`"/>
            </v-hover>
            </a> or on
            <a class="no-underline" href="https://twitter.com/Martin_Heinz_" target="_blank">
                <v-hover>
                    <font-awesome-icon :icon="['fab', 'twitter']" @mouseover="next_active = true" @mouseout="next_active = false"
                                       slot-scope="{ hover }"
                                       :class="`${hover? 'icon-active': 'icon-inactive'}`"/>
                </v-hover>
            </a>.
            </p>

        <p>
            On this page you can find some information about me and a few blog posts I wrote. Most of them are about topics that I'm most interested in,
            such as cryptography, serverless and distributed technologies, or about programming languages like Python or Go. I like to read a lot books,
            so you might also find my opinions or review of some them here.
        </p>

        <p>
            I'm also posting my blog posts on <a href="https://dev.to/Panda-ManR">DEV.to</a> and <a href="https://medium.com/@martin.heinz">Medium</a>,
            so you can find them there as well.
        </p>

        <div id="cols" class="row">
            <div class="column">
                <h2><font-awesome-icon icon="heartbeat"/> Life so far...</h2>
                <ul class="about-list">
                    <li>Breathing since 1994</li>
                    <li>Started studying CS in 2014</li>
                    <li>Got Bachelors in 2017</li>
                    <li>Started working at IBM in 2018</li>
                    <li>Got Masters with honours in 2019</li>
                </ul>
            </div>
            <div class="column">
                <h2><font-awesome-icon icon="fire"/> Passionate about...</h2>
                <ul class="about-list">
                    <li>Food</li>
                    <li>Books</li>
                    <li>Weight Lifting</li>
                    <li>Coding</li>
                    <li>Music</li>
                </ul>
            </div>
            <div class="column">
                <h2><font-awesome-icon icon="lightbulb"/> Thinking about...</h2>
                <ul class="about-list">
                    <li>Cloud-Native Apps</li>
                    <li>Cryptography</li>
                    <li>Testing</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'About',
};
</script>

<style>
    .custom-btn::before {
        color: transparent
    }

    .custom-btn:hover {
        color: #d480aa;
        min-width: 0;
    }

    .no-underline {
        background-image: none !important;
    }

    .column {
        float: left;
        width: 33%;
        padding: 10px;
        height: 50%;
    }

    /* Clear floats after the columns */
    .row:after {
        content: "";
        display: table;
        clear: both;
    }

    .about-list {
        padding-left: 12px;
    }

    @media (min-width: 320px) and (max-width: 600px) {
        #cols .column {
            width: 100%;
        }
    }
</style>
