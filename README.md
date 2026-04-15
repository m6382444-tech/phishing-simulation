<!DOCTYPE html>
<html>
<head>
    <title>Login Page</title>
</head>
<body>

<h2>Login</h2>

<form onsubmit="countSubmission()">
    <input type="text" placeholder="Username" required><br><br>
    <input type="password" placeholder="Password" required><br><br>
     <button onclick="countSubmission(); alert('This is a simulation and was created for educational purposes only.')">sign in</button>
            
    </form>

<p>Total Submissions: <span id="count">0</span></p>

<script>
let count = localStorage.getItem("submissionCount") || 0;
document.getElementById("count").innerText = count;

function countSubmission() {
    count++;
    localStorage.setItem("submissionCount", count);
    document.getElementById("count").innerText = count;
}
</script>

</body>
</html>
