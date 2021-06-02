<script>
    let phoneGood = true
    const handlePhone = (e) => {
        let phoneno =  /^\(?([0-9]{3})\)?[-. ]?([0-9]{3})[-. ]?([0-9]{4})$/;
        if((e.target.value.match(phoneno))){
            
            return phoneGood = true
        }else {
            console.log(phoneno)
            alert('Please only enter numbers 10 digits no space')
            e.target.placeholder = "Enter a ten-digit number without space"
            e.target.value = ''
            e.target.focus();
            return phoneGood =  false
        }
    }
</script>


<div class="formWrap">
    <div class="quoteTop">
        <h2>Thank you for your interest in Big Tex Metal Buildings!</h2>
        <p>
            Please give us a call or find the style and number you are
            interested in and fill out the form below.
        </p>
    </div>
    <form action="https://formspree.io/f/moqydnnr" method="POST">
        <input class:dontwork={!phoneGood} type="text" name="name" placeholder="Full Name" required />
        <input class:dontwork={!phoneGood} type="email" name="_replyto" placeholder="Email" required />
        <input type="text" name="phone" id="phone" placeholder="Phone Number" required on:change={handlePhone}>
        <textarea class:dontwork={!phoneGood} name="message"rows="4" cols="50"  placeholder="Message (Please reference the style and number of building you are interested in)" required />

        <!-- your other form fields go here -->

        <button type="submit">Send</button>
    </form>
</div>

<style>
    .dontwork{
        pointer-events: none;
        background-color: red;
    }
    .quoteTop {
        width: 100%;
        text-align: center;
    }
    .formWrap {
        width: 100%;
        padding: 100px 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 65vh;
    }

    form {
        width: 50%;
        /* border:1px solid #152749; */
        padding: 20px;
        display: grid;
        margin-bottom: 100px;
        background: #152749;
    }

    @media only screen and (max-width: 768px) {
        form {
            width: 90%;
            padding: 5px;
        }

        h2 {
            font-size: 1.2rem;
            width: 70%;
            margin: 0 auto;
        }

        p {
            width: 70%;
            margin: 0 auto;
            font-size: 1rem;
            padding: 20px 0;
        }
    }
</style>
