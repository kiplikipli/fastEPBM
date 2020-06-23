# fastEPBM

## Source Code

```javascript
const content = document.getElementsByClassName("content");
const formMK = content[1];
const formDosen = content[2].querySelectorAll(".panel-warning");
const mkQuestions = formMK.querySelectorAll(".panel-danger");

function selectRadio(question) {
	var random = Math.floor(Math.random() * (3 - 2 + 1)) + 2;
	$(question.getElementsByTagName("input").item(random)).prop(
		"checked",
		true
	);
}

// For courses questions
mkQuestions.forEach((mkQuestion) => {
	selectRadio(mkQuestion);
});

// For lecturers questions
formDosen.forEach((dosen) => {
	let dosenQuestions = dosen.querySelectorAll(".panel-danger");
	dosenQuestions.forEach((dosenQuestion) => {
		selectRadio(dosenQuestion);
	});
});

// Final statement
$("#Pernyataan").prop("checked", true);

```

## How to Use
1. Open EPBM page in SIMAK
2. Open Web Console in browser ( Ctrl + Shift + I ) in Google Chrome
3. Copy that code 
4. Voila your EPBM filled with random between "Setuju" and "Sangat Setuju"
