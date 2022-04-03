<script>
    let password = '';
    let username = '';

    const login = () => alert(`Login button Pressed!`);
    const signup = () => alert(`Signup button Pressed!`);
</script>

<section>
    <form on:submit|preventDefault={login}>
        <label>
            Username
            <input required bind:value={username}>
        </label>
        <label>
            Password
            <input required bind:value={password}>
        </label>
        <div class="buttons">
            <button>Login</button>
            <button type="button" on:click={signup}>Sign up</button>
        </div>
    </form>
</section>

<style>
    .buttons{
        display: flex;
        justify-content: space-between;
        font-size: 1.5rem;
        margin-top: 1rem;
    }

    form {
        display: inline-block;
    }

    input {
        display: block;
        margin-top: 0.3rem;
    }

    label {
        color: white;
        display: block;
        font-size: 1.5rem;
        margin-top: 0.5rem;
    }

    label {
        display: block;
    }

    input, button, select, textarea {
        font-family: inherit;
        font-size: inherit;
        -webkit-padding: 0.4em 0;
        padding: 0.4em;
        margin: 0 0 0.5em 0;
        box-sizing: border-box;
        border: 1px solid #ccc;
        border-radius: 2px;
    }

    input:disabled {
        color: #ccc;
    }

    input:invalid {
        box-shadow: none;
    }

    button {
        color: #333;
        background-color: #f4f4f4;
        outline: none;
    }

    button:disabled {
        color: #999;
    }

    button:not(:disabled):active {
        background-color: #ddd;
    }

    button:focus {
        border-color: #666;
    }
</style>