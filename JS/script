// Donor Registration
document.getElementById('donorForm').addEventListener('submit', function (e) {
    e.preventDefault();
    
    const donor = {
      name: document.getElementById('name').value,
      bloodGroup: document.getElementById('bloodGroup').value,
      location: document.getElementById('location').value,
      contact: document.getElementById('contact').value
    };
  
    let donors = JSON.parse(localStorage.getItem('donors')) || [];
    donors.push(donor);
    localStorage.setItem('donors', JSON.stringify(donors));
  
    alert('Thank you for registering as a donor!');
    document.getElementById('donorForm').reset();
  });
  
  // Find Donor
  document.getElementById('searchForm').addEventListener('submit', function (e) {
    e.preventDefault();
    
    const bloodGroup = document.getElementById('searchBloodGroup').value;
    const donors = JSON.parse(localStorage.getItem('donors')) || [];
    const matchingDonors = donors.filter(donor => donor.bloodGroup === bloodGroup);
  
    const donorList = document.getElementById('donorList');
    donorList.innerHTML = '';
  
    if (matchingDonors.length > 0) {
      matchingDonors.forEach(donor => {
        const donorInfo = document.createElement('div');
        donorInfo.innerHTML = `
          <p><strong>Name:</strong> ${donor.name}</p>
          <p><strong>Location:</strong> ${donor.location}</p>
          <p><strong>Contact:</strong> ${donor.contact}</p>
          <hr>
        `;
        donorList.appendChild(donorInfo);
      });
    } else {
      donorList.innerHTML = '<p>No donors found for this blood group.</p>';
    }
  });
  
  // Request Blood
  document.getElementById('requestForm')?.addEventListener('submit', function (e) {
    e.preventDefault();
    
    const request = {
      patientName: document.getElementById('patientName').value,
      requiredBloodGroup: document.getElementById('requiredBloodGroup').value,
      hospitalLocation: document.getElementById('hospitalLocation').value,
      contact: document.getElementById('contact').value
    };
  
    alert('Blood request submitted successfully!');
    document.getElementById('requestForm').reset();
  });
