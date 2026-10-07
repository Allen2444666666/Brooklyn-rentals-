<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Brooklyn's Rentals</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f1ea;
      margin: 0;
      color: #1d1d1d;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 24px;
    }

    .hero {
      background: linear-gradient(135deg, #efe6d8, #e3f0ed);
      padding: 50px 0;
    }

    h1 {
      font-size: 42px;
      margin: 10px 0;
    }

    .tag {
      color: #2d6a4f;
      font-weight: bold;
      letter-spacing: 2px;
      text-transform: uppercase;
      font-size: 12px;
    }

    .card {
      background: white;
      padding: 24px;
      border-radius: 18px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
      margin-top: 30px;
    }

    form {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    .full {
      grid-column: 1 / -1;
    }

    label {
      display: block;
      margin-bottom: 8px;
      font-weight: bold;
    }

    input,
    select,
    textarea,
    button {
      width: 100%;
      padding: 12px;
      border-radius: 10px;
      border: 1px solid #d6cfc4;
      font-size: 16px;
      box-sizing: border-box;
    }

    textarea {
      min-height: 110px;
      resize: vertical;
    }

    .check {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 10px;
    }

    .check input {
      width: auto;
    }

    button {
      background: #2d6a4f;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
    }

    button:hover {
      background: #24563f;
    }

    .result {
      display: none;
      background: #edf9f0;
      border: 1px solid #d0e8d6;
      padding: 18px;
      border-radius: 12px;
      margin-top: 18px;
    }

    @media (max-width: 700px) {
      form {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: 32px;
      }
    }
  </style>
</head>

<body>

  <header class="hero">
    <div class="container">

      <div class="tag">
        Find your next Brooklyn home
      </div>

      <h1>
        Brooklyn's Rentals
      </h1>

      <p>
        Tell us what you need and we’ll match you with the right apartment.
      </p>

    </div>
  </header>


  <div class="container">

    <div class="card">

      <form id="rentalForm">

        <!-- FULL NAME -->
        <div>
          <label for="fullName">
            Full name
          </label>

          <input
            id="fullName"
            type="text"
            name="fullName"
            required
          >
        </div>


        <!-- EMAIL -->
        <div>
          <label for="email">
            Email address
          </label>

          <input
            id="email"
            type="email"
            name="email"
            required
          >
        </div>


        <!-- BUDGET -->
        <div>
          <label for="budget">
            Monthly budget
          </label>

          <select
            id="budget"
            name="budget"
            required
          >

            <option value="">
              Select
            </option>

            <option>
              $500 - $1,000
            </option>

            <option>
              $1,000 - $1,500
            </option>

            <option>
              $1,500 - $2,000
            </option>

            <option>
              $2,000 - $2,500
            </option>

            <option>
              $2,500 - $3,500
            </option>

            <option>
              $3,500 - $5,000
            </option>

            <option>
              $5,000+
            </option>

          </select>
        </div>


        <!-- CREDIT SCORE -->
        <div>
          <label for="credit-score">
            My credit-score
          </label>

          <select
            id="credit-score"
            name="credit-score"
            required
          >

            <option value="">
              Select
            </option>

            <option>
              &lt; 100
            </option>

            <option>
              101 - 200
            </option>

            <option>
              201 - 300
            </option>

            <option>
              301 - 400
            </option>

            <option>
              401 - 500
            </option>

            <option>
              501 - 600
            </option>

            <option>
              601 - 700
            </option>

            <option>
              701 - 800
            </option>

            <option>
              801 - 900
            </option>

            <option>
              901 - 1000
            </option>

          </select>
        </div>


        <!-- BEDROOMS -->
        <div>
          <label for="bedrooms">
            Bedrooms
          </label>

          <select
            id="bedrooms"
            name="bedrooms"
            required
          >

            <option value="">
              Select
            </option>

            <option>
              Studio
            </option>

            <option>
              1 bedroom
            </option>

            <option>
              2 bedrooms
            </option>

            <option>
              3 bedrooms
            </option>

            <option>
              4+ bedrooms
            </option>

          </select>
        </div>


        <!-- MOVE IN -->
        <div>
          <label for="moveIn">
            Move-in month
          </label>

          <input
            id="moveIn"
            type="month"
            name="moveIn"
            required
          >
        </div>


        <!-- LIFESTYLE -->
        <div class="full">

          <label for="lifestyle">
            Lifestyle priorities
          </label>

          <textarea
            id="lifestyle"
            name="lifestyle"
            placeholder="Example: quiet, pet-friendly, gym nearby, walkable neighborhood..."
          ></textarea>

        </div>


        <!-- AMENITIES -->
        <div class="full">

          <label>
            Must-have amenities
          </label>

          <div class="check">

            <input
              type="checkbox"
              name="amenity"
              value="Laundry"
            >

            Laundry

          </div>


          <div class="check">

            <input
              type="checkbox"
              name="amenity"
              value="Gym"
            >

            Gym

          </div>


          <div class="check">

            <input
              type="checkbox"
              name="amenity"
              value="Doorman"
            >

            Doorman

          </div>


          <div class="check">

            <input
              type="checkbox"
              name="amenity"
              value="Pet friendly"
            >

            Pet friendly

          </div>

        </div>


        <!-- SUBMIT -->
        <div class="full">

          <button type="submit">
            Submit survey
          </button>

        </div>

      </form>


      <!-- RESULT -->
      <div
        id="result"
        class="result"
      >

        <strong>
          Your rental profile:
        </strong>

        <p id="profile"></p>

      </div>

    </div>

  </div>


  <script>

    document
      .getElementById("rentalForm")
      .addEventListener("submit", async function (e) {

        e.preventDefault();


        const name =
          document.getElementById("fullName").value;

        const email =
          document.getElementById("email").value;

        const budget =
          document.getElementById("budget").value;

        const credit =
          document.getElementById("credit-score").value;

        const bedrooms =
          document.getElementById("bedrooms").value;

        const moveIn =
          document.getElementById("moveIn").value;

        const lifestyle =
          document.getElementById("lifestyle").value;


        const amenities =
          [
            ...document.querySelectorAll(
              "input[name='amenity']:checked"
            )
          ].map(
            item => item.value
          );


        const selectedAmenities =
          amenities.length
            ? amenities.join(", ")
            : "No specific amenities selected";


        const lifestyleText =
          lifestyle ||
          "comfortable and convenient living";


        const resultText =
          `${name} (${email}) is looking for a ${bedrooms} apartment with a ${budget} budget. Their credit-score range is ${credit}. They want to move in ${moveIn}. Lifestyle priorities: ${lifestyleText}. Amenities: ${selectedAmenities}.`;


        const formData =
          new FormData();


        formData.append(
          "name",
          name
        );

        formData.append(
          "email",
          email
        );

        formData.append(
          "budget",
          budget
        );

        formData.append(
          "credit-score",
          credit
        );

        formData.append(
          "bedrooms",
          bedrooms
        );

        formData.append(
          "moveIn",
          moveIn
        );

        formData.append(
          "lifestyle",
          lifestyleText
        );

        formData.append(
          "amenities",
          selectedAmenities
        );


        formData.append(
          "_subject",
          "New Brooklyn's Rentals Survey"
        );

        formData.append(
          "_captcha",
          "false"
        );

        formData.append(
          "_template",
          "table"
        );


        try {

          const response =
            await fetch(
              "https://formsubmit.co/brooklynhousing64@gmail.com",
              {
                method: "POST",
                body: formData
              }
            );


          if (!response.ok) {

            throw new Error(
              "Survey could not be sent."
            );

          }


          document.getElementById(
            "profile"
          ).textContent =
            resultText;


          document.getElementById(
            "result"
          ).style.display =
            "block";


          this.reset();


        } catch (error) {

          alert(
            "There was a problem sending the survey. Please try again."
          );

          console.error(error);

        }

      });

  </script>

</body>
</html>
