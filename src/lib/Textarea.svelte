<script>
    export let label;
    export let id;
</script>

<label class="form-label input-textfield" for={id}>
    <span class="star">{label}</span>

    <textarea aria-required="true" cols="5" placeholder="" required
              rows="1"></textarea>
</label>
<style>
    form {
        color: var(--grey);
    }

    fieldset {
        border: none;
    }

    legend {
        position: absolute;
        top: 0;
        left: -9999px;
    }

    label {
        margin-top: 1.8rem;
        display: grid;
        width: 100%;
        border-bottom: 1.5px solid var(--black);
        gap: 0.8rem;
    }

    span {
        grid-row: 1;
        grid-column: 1;
        height: 2rem;

    }

    input {
        grid-row: 2;
        grid-column-start: 1;
        grid-column-end: 3;
    }


    input {
        border: none;
    }


    textarea {
        height: auto;
        border: none;
    }

    .star:after {
        content: "*";
        font-size: 2rem;
        color: red;

    }

    .no-star:after {
        font-size: 2rem;

        content: "";
    }


    /*ui states*/
    input:focus, textarea:focus, select:focus, option:focus {
        outline: 2px solid var(--blue);
    }

    textarea {
        width: 100%; /* Make it full width */
    }

    /* form focus valid  */

    input[type='text']:user-valid,
    input[type='email']:valid,
    input[type='number']:valid,
    textarea:user-valid,
    select:user-valid {
        outline: 2px solid green;

    }

    /* form focus invalid */

    input[type='text']:user-invalid,
    input[type='email']:user-invalid,
    input[type='number']:user-invalid,
    textarea:user-invalid,
    select:user-invalid {
        outline: 2px solid red;
    }


    /*contianer queries */
    form {
        container-type: inline-size;
    }

    @container  (min-width: 600px) {
        fieldset {
            display: grid;
            grid-template-columns: auto auto;
            max-width: 700px;
            gap: 1rem;

        }

        .input-textfield {
            grid-row: 6;
            grid-column-start: 1;
            grid-column-end: 3;
        }

        .dropown {
            grid-row: 7;
        }
    }
</style>