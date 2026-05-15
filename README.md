# Swiftsync
This is my first repository about the first capstone project of our college IIT PATNA.
<br>
Author - Subahu Ranjan Sahoo
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SwiftSync AI - Join the Movement</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
</head>
<body class="bg-gray-50">

  <div class="max-w-2xl mx-auto mt-10 p-8 bg-white rounded-2xl shadow-xl">
    <div class="text-center mb-8">
      <h1 class="text-3xl font-bold text-emerald-600">SwiftSync AI</h1>
      <p class="text-gray-600 mt-2">Connecting Surplus to Service</p>
      <h2 class="text-xl font-semibold mt-6 text-gray-800">Join the Movement</h2>
    </div>

    <form id="joinForm" class="space-y-6">

      <!-- Role Selection -->
      <div>
        <label class="block text-gray-700 font-medium mb-3">I want to:</label>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-3">
          <label class="flex items-center gap-2 border rounded-xl p-4 cursor-pointer hover:border-emerald-500 transition">
            <input type="radio" name="role" value="donor" class="w-4 h-4 accent-emerald-600" required>
            <span class="font-medium">Donate</span>
          </label>
          <label class="flex items-center gap-2 border rounded-xl p-4 cursor-pointer hover:border-emerald-500 transition">
            <input type="radio" name="role" value="receiver" class="w-4 h-4 accent-emerald-600">
            <span class="font-medium">Receive Help</span>
          </label>
          <label class="flex items-center gap-2 border rounded-xl p-4 cursor-pointer hover:border-emerald-500 transition">
            <input type="radio" name="role" value="volunteer" class="w-4 h-4 accent-emerald-600">
            <span class="font-medium">Volunteer</span>
          </label>
          <label class="flex items-center gap-2 border rounded-xl p-4 cursor-pointer hover:border-emerald-500 transition">
            <input type="radio" name="role" value="ngo" class="w-4 h-4 accent-emerald-600">
            <span class="font-medium">NGO</span>
          </label>
        </div>
      </div>

      <!-- Basic Info -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
          <input type="text" name="full_name" required
                 class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                 placeholder="Your Name">
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">Phone Number</label>
          <input type="tel" name="phone" required
                 class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                 placeholder="63722 52530">
        </div>
      </div>

      <div>
        <label class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
        <input type="email" name="email" required
               class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
               placeholder="you@example.com">
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">Create Password</label>
          <input type="password" name="password" required
                 class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                 placeholder="••••••••">
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">Confirm Password</label>
          <input type="password" name="confirm_password" required
                 class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                 placeholder="••••••••">
        </div>
      </div>

      <!-- Gender -->
      <div>
        <label class="block text-sm font-medium text-gray-700 mb-2">Gender</label>
        <div class="flex gap-6">
          <label><input type="radio" name="gender" value="male" class="mr-2"> Male</label>
          <label><input type="radio" name="gender" value="female" class="mr-2"> Female</label>
          <label><input type="radio" name="gender" value="other" class="mr-2"> Other</label>
        </div>
      </div>

      <!-- Location -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">City</label>
          <select name="city" required
                  class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500">
            <option value="">Select City</option>
            <option value="Patna">Patna</option>
            <option value="Lucknow">Lucknow</option>
            <option value="Mumbai">Mumbai</option>
            <option value="Pune">Pune</option>
            <option value="Delhi NCR">Delhi NCR</option>
            <option value="Kolkata">Kolkata</option>
            <option value="Bhubaneswar">Bhubaneswar</option>
            <option value="Hyderabad">Hyderabad</option>
            <option value="Bangalore">Bangalore</option>
            <option value="Chennai">Chennai</option>
          </select>
        </div>
        <div>
          <label class="block text-sm font-medium text-gray-700 mb-1">Area / Locality</label>
          <input type="text" name="area" required
                 class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                 placeholder="e.g. Laxmi Nagar, Delhi">
        </div>
      </div>

      <!-- Role-specific Fields will appear here via JS -->
      <div id="roleFields"></div>

      <!-- Why Join -->
      <div>
        <label class="block text-sm font-medium text-gray-700 mb-1">Why do you want to join SwiftSync AI?</label>
        <textarea name="message" rows="4"
                  class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:outline-none focus:border-emerald-500"
                  placeholder="I have surplus food every weekend... OR My community needs regular support..."></textarea>
      </div>

      <button type="submit"
              class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-semibold py-4 rounded-xl text-lg transition">
        Join SwiftSync AI
      </button>
    </form>
  </div>

  <script>
    // Simple role-based field display
    document.querySelectorAll('input[name="role"]').forEach(radio => {
      radio.addEventListener('change', function() {
        const container = document.getElementById('roleFields');
        container.innerHTML = '';

        if (this.value === 'donor') {
          container.innerHTML = `
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">What would you like to donate?</label>
              <div class="grid grid-cols-2 gap-3">
                <label class="flex items-center gap-2"><input type="checkbox" name="items" value="food"> Surplus Food</label>
                <label class="flex items-center gap-2"><input type="checkbox" name="items" value="clothes"> Clothes</label>
                <label class="flex items-center gap-2"><input type="checkbox" name="items" value="essentials"> Daily Essentials</label>
                <label class="flex items-center gap-2"><input type="checkbox" name="items" value="other"> Other</label>
              </div>
            </div>`;
        } 
        else if (this.value === 'receiver') {
          container.innerHTML = `
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">What do you need help with?</label>
              <div class="grid grid-cols-2 gap-3">
                <label class="flex items-center gap-2"><input type="checkbox" name="needs" value="food"> Food</label>
                <label class="flex items-center gap-2"><input type="checkbox" name="needs" value="clothes"> Clothes</label>
                <label class="flex items-center gap-2"><input type="checkbox" name="needs" value="essentials"> Essentials</label>
              </div>
            </div>`;
        }
      });
    });
  </script>
</body>
</html>
