  const form = document.querySelector('form');
    form.addEventListener('submit', (event) => {
      event.preventDefault();

      const carMileage = parseFloat(document.getElementById('car-mileage').value);
      const carDistance = parseFloat(document.getElementById('car-distance').value);
      const electricityUsage = parseFloat(document.getElementById('electricity-usage').value);
      const gasUsage = parseFloat(document.getElementById('gas-usage').value);
      const wasteProduced = parseFloat(document.getElementById('waste-produced').value);

      const carbonFootprint = (carDistance / carMileage) + electricityUsage + gasUsage + wasteProduced;

      alert(`Your carbon footprint is ${carbonFootprint.toFixed(2)} tons of CO2 equivalent.`);
    });
