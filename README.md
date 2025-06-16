# Mines-Predictor
Mines Predictor 1 win
function predictSafeTiles(mineCount) {
  const gridSize = 25;
  let safeTiles = [];
  for (let i = 0; i < gridSize - mineCount; i++) {
    let rand = Math.floor(Math.random() * gridSize);
    while (safeTiles.includes(rand)) {
      rand = Math.floor(Math.random() * gridSize);
    }
    safeTiles.push(rand);
  }
  return safeTiles;
}
