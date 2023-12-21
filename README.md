<fieldset>
  <label>
    <input role="switch" type="checkbox" />
    <span>알람</span>
  </label>
  <label>
    <input role="switch" type="checkbox" disabled />
    <span>알람 (비활성화)</span>
  </label>
</fieldset>


label {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  cursor: pointer;
}

[type="checkbox"] {
  appearance: none;
  position: relative;
  border: max(2px, 0.1em) solid gray;
  border-radius: 1.25em;
  width: 2.25em;
  height: 1.25em;
}

[type="checkbox"]::before {
  content: "";
  position: absolute;
  left: 0;
  width: 1em;
  height: 1em;
  border-radius: 50%;
  transform: scale(0.8);
  background-color: gray;
  transition: left 250ms linear;
}

[type="checkbox"]:checked {
  background-color: tomato;
  border-color: tomato;
}

[type="checkbox"]:checked::before {
  background-color: white;
  left: 1em;
}

[type="checkbox"]:disabled {
  border-color: lightgray;
  opacity: 0.7;
  cursor: not-allowed;
}

[type="checkbox"]:disabled:before {
  background-color: lightgray;
}

[type="checkbox"]:disabled + span {
  opacity: 0.7;
  cursor: not-allowed;
}

[type="checkbox"]:focus-visible {
  outline-offset: max(2px, 0.1em);
  outline: max(2px, 0.1em) solid tomato;
}

[type="checkbox"]:enabled:hover {
  box-shadow: 0 0 0 max(4px, 0.2em) lightgray;
}

/* Global CSS */
body {
  display: grid;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

fieldset {
  border: none;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}
