<template>
    <v-app>
        <Container id="container" width="8">
            <Container width="3" height="4">
                <SwordGroup />
                <ShieldGroup />
                <TunicGroup />
                <BootsGroup />
            </Container>

            <Container width="5" height="3">
                <Container width="4" height="3">
                    <Container width="3" height="2">
                        <StickGroup />
                        <NutGroup />
                        <BoomerangGroup />
                        <SlingshotGroup />
                        <HammerGroup />
                        <LensGroup />
                    </Container>

                    <ExplosivesGroup />
                    <BowGroup />
                </Container>

                <SpellsGroup />
            </Container>

            <HookshotGroup />
            <OcarinaGroup />
            <BottleGroup />
            <BeanGroup />
            <PoeGroup />

            <Container width="8" height="1">
                <UpgradesGroup />
                <CollectiblesGroup />
            </Container>

            <Container width="5" height="1" id="specials">
                <ChildTradeGroup />
                <AdultTradeGroup />
                <LetterGroup />
                <GerudoTokenGroup />
                <AgonyGroup />
            </Container>

            <Container width="6" height="2" id="songs">
                <UtilitySongGroup />
                <WarpSongGroup />
            </Container>

            <Container id="dungeons">
                <Container id="adult" unit_size="40">
                    <AdultDungeonGroup />
                </Container>

                <Container id="child" unit_size="40">
                    <ChildDungeonGroup />
                </Container>
            </Container>
        </Container>
    </v-app>
</template>

<script>

let fs = window.require('fs');

let components = {};

function recur(path) {
    let dir = fs.readdirSync(`./src/${path}`);
    for (let d = 0; d < dir.length; d++) {
        let isDir = fs.statSync(`./src/${path}/${dir[d]}`).isDirectory();
        if (isDir) { recur(`${path}/${dir[d]}`) }
        else { components[dir[d].split('.')[0]] = require(`./${path}/${dir[d]}`).default }
    }
}

recur('components');

export default {
    name: 'App',

    components: components,

    data: () => ({}), 
}
</script>

<style>
    html {
        overflow-y: hidden !important;
    }

    @font-face {
        font-family: 'square';
        src: local('square'), url(./assets/Square.ttf) format('truetype');
    }

    .v-application {
        line-height: 0.5 !important;
    }

    .v-application--wrap {
        flex-direction: row !important;
    }

    #container {
        background-color: #00FF0099;
        margin: auto;
    }

    #specials {
        margin: 10px 52px;
    }

    #songs {
        margin: 0 35px;
    }

    #dungeons {
        margin: 10px 0;
    }

    #dungeons #adult {
        margin: 0 20px;
    }

    #dungeons #child {
        margin: 0 80px;
    }
</style>
