<!DOCTYPE html>
<html>
<head>
<title>MM Video AI</title>
</head>
<body>

<h1>MM Video AI</h1>

<p>Upload Video</p>
<input type="file" id="videoFile" accept="video/*">

<br><br>

<video id="preview" width="320" controls></video>

<br><br>

<button onclick="previewVideo()">Preview Video</button>

<script>
function previewVideo() {
  const file = document.getElementById('videoFile').files[0];

  if (!file) {
    alert('Video ရွေးပါ');
    return;
  }

  const url = URL.createObjectURL(file);
  document.getElementById('preview').src = url;
}
</script>

</body>
</html>
