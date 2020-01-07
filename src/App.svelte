<script>
  import Note from "./components/Note.svelte";
</script>

<style>
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  body {
    background-color: #143f6b;
    margin: 0;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .piano {
    display: flex;
  }
</style>

<div class="piano">
  <Note note={'C'} color={'white'} audioSrc="notes/C.mp3" keyCode={'z'} />
  <Note note={'Db'} color={'black'} audioSrc="notes/Db.mp3" keyCode={'s'} />
  <Note note={'D'} color={'white'} audioSrc="notes/D.mp3" keyCode={'x'} />
  <Note note={'Eb'} color={'black'} audioSrc="notes/Eb.mp3" keyCode={'d'} />
  <Note note={'E'} color={'white'} audioSrc="notes/E.mp3" keyCode={'c'} />
  <Note note={'F'} color={'white'} audioSrc="notes/F.mp3" keyCode={'v'} />
  <Note note={'Gb'} color={'black'} audioSrc="notes/Gb.mp3" keyCode={'g'} />
  <Note note={'G'} color={'white'} audioSrc="notes/G.mp3" keyCode={'b'} />
  <Note note={'Ab'} color={'black'} audioSrc="notes/Ab.mp3" keyCode={'h'} />
  <Note note={'A'} color={'white'} audioSrc="notes/A.mp3" keyCode={'n'} />
  <Note note={'Bb'} color={'black'} audioSrc="notes/Bb.mp3" keyCode={'j'} />
  <Note note={'B'} color={'white'} audioSrc="notes/B.mp3" keyCode={'m'} />
</div>
