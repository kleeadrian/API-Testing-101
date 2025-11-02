# API-Testing-101

Exercises 1 - Tests to be created


_pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});_



_pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});_


