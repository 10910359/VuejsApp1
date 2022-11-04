<template>
    <div id="app">
        <h1>Text to speech reader</h1>
        <form action="/" method="post">
            <table class="calc">
                <tbody>
                    <tr>
                        <td><label for="text">Enter text here</label></td>
                    </tr>
                    <tr>
                        <td>
                            <textarea id="area" prefix="area" :style="{fontSize: '${fontsize}px'}" rows="10" v-model="area" class="form-control" autofocus></textarea>

                        
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <button type="button" @click="SpeechForm.playbtn()" class="btn btn-default">
                                <i class="glyphicon glyphicon-play"></i>
                                Play
                            </button>

                            <button type="button" @click="SpeechForm.stopbtn()" class="btn btn-default">
                                <i class="glyphicon glyphicon-stop"></i>
                                Stop
                            </button>

                            <button type="button" @click="SpeechForm.resetform()" class="btn btn-default">
                                <i class="glyphicon glyphicon-remove"></i>
                                Clear
                            </button>

                            <button type="button" @click="SpeechForm.copy()" class="btn btn-default">
                                <i class="glyphicon glyphicon-duplicate"></i>
                                Copy
                            </button>


                            <button type="button" @click="SpeechForm.zoomin()" class="btn btn-default">
                                <i class="glyphicon glyphicon-zoom-in"></i>
                                Zoom in
                            </button>


                            <button type="button" @click="SpeechForm.zoomout()" class="btn btn-default">
                                <i class="glyphicon glyphicon-zoom-out"></i>
                                Zoom out
                            </button>

                            
                            <Select v-model="voiceIdx" :options="voices" />



                        </td>
                    </tr>
                </tbody>
                  
            </table>
        </form>
        <Home msg="" />
    </div>
</template>

<script>
    import Home from './components/Home.vue';

    export default {
        name: 'app',
        components: {
            Home
        }
    };
</script>

<style>
</style>

