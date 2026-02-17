$user = \App\Models\User::create([
'name' => 'Eloquent Expert',
'email' => 'eloquent@expert.com',
'password' => bcrypt('password')
]);

// Create a chirp for this user
$chirp = $user->chirps()->create([
'message' => 'Eloquent makes database work a breeze!'
]);

// User 1 - 1 Note
$user1 = \App\Models\User::create([
    'name' => 'Solo Singer',
    'email' => 'solo@example.com',
    'password' => bcrypt('password')
]);
$user1->chirps()->create(['message' => 'My one and only note.']);

// User 2 - 2 Notes
$user2 = \App\Models\User::create([
    'name' => 'Double Talker',
    'email' => 'double@example.com',
    'password' => bcrypt('password')
]);
$user2->chirps()->create(['message' => 'First of two!']);
$user2->chirps()->create(['message' => 'Second of two!']);

// User 3 - 3 Notes
$user3 = \App\Models\User::create([
    'name' => 'Triple Threat',
    'email' => 'triple@example.com',
    'password' => bcrypt('password')
]);
$user3->chirps()->create(['message' => 'Starting the trio.']);
$user3->chirps()->create(['message' => 'The middle child.']);
$user3->chirps()->create(['message' => 'The final note.']);

Invoke controller has only one function
while Resource controller has the 5 http requests
