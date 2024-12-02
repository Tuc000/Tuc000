const express = require('express');
const app = express();
app.use(express.json());

app.post('/save-location', (req, res) => {
    const { latitude, longitude } = req.body;
    console.log(`Received location: ${latitude}, ${longitude}`);
    res.send('Location saved!');
});

app.listen(3000, () => console.log('Server running on port 3000'));
