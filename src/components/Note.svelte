<script>
  export let note,
    color = "white",
    audioSrc,
    isActive = false,
    keyCode;

  const playNote = key => {
    const noteAudio = new Audio(audioSrc);
    noteAudio.currentTime = 0;
    noteAudio.play();
    isActive = true;

    noteAudio.addEventListener("ended", () => {
      isActive = false;
    });
  };

  document.addEventListener("keydown", e => {
    if (e.repeat) return;
    if (e.key === keyCode) playNote(e.key);
  });
</script>

<style type="text/scss">
  .key {
    height: calc(var(--width) * 4);
    width: var(--width);
    border-radius: 0 0 4px 4px;
    cursor: pointer;
    display: flex;
  }

  .white {
    --width: 80px;
    background-color: #f6f5f3;
    border: 1px solid #888;
  }

  .white + .white {
    margin-left: 2px;
  }

  .black {
    --width: 48px;
    background-color: #555;
    border: 1px solid #fff;
    border-top-color: transparent;
    margin-left: calc(var(--width) / -2);
    margin-right: calc(var(--width) / -2);
    z-index: 2;
  }

  .white.active,
  .black.active {
    background-color: #3ac8da;
  }

  .key-note-label {
    flex: 1 1;
    align-self: flex-end;
    text-align: center;
    text-transform: capitalize;
    font-size: 18px;
    line-height: 60px;
    color: #888;
  }

  .black .key-note-label {
    color: #f8e8d5;
  }

  .key.active .key-note-label {
    color: #f8e8d5;
  }
</style>

<div class="key {color}" class:active={isActive} on:click={playNote(note)}>
  <div class="key-note-label">{note}</div>
</div>
