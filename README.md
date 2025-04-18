<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نظام تسجيل المواعيد</title>
<script src="https://cdn.tailwindcss.com/3.4.16"></script>
<script>tailwind.config={theme:{extend:{colors:{primary:'#4f46e5',secondary:'#6366f1'},borderRadius:{'none':'0px','sm':'4px',DEFAULT:'8px','md':'12px','lg':'16px','xl':'20px','2xl':'24px','3xl':'32px','full':'9999px','button':'8px'}}}}</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/remixicon@4.5.0/fonts/remixicon.css" rel="stylesheet">
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
body {
font-family: 'Cairo', sans-serif;
background-color: #f9fafb;
}
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
-webkit-appearance: none;
margin: 0;
}
input[type=number] {
-moz-appearance: textfield;
}
</style>
</head>
<body class="min-h-screen">
<div class="container mx-auto px-4 py-8 max-w-4xl">
<header class="mb-8 text-center">
<h1 class="text-3xl font-bold text-gray-800 mb-2">نظام تسجيل المواعيد</h1>
<p class="text-gray-600">سجل بياناتك بسهولة وسرعة</p>
</header>
<div class="bg-white rounded-lg shadow-md p-6 mb-8">
<h2 class="text-xl font-semibold text-gray-800 mb-6">إدخال البيانات</h2>
<form id="appointmentForm" class="space-y-6" action="https://formspree.io/f/xanegoyq" method="POST">
<div>
<label for="email" class="block text-sm font-medium text-gray-700 mb-2">البريد الإلكتروني</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-mail-line"></i>
</div>
</div>
<input type="email" id="email" name="email" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل البريد الإلكتروني">
</div>
</div>

<div>
<label for="message" class="block text-sm font-medium text-gray-700 mb-2">رسالة إضافية</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 top-3 flex items-start pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-message-2-line"></i>
</div>
</div>
<textarea id="message" name="message" rows="4"
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل أي ملاحظات إضافية"></textarea>
</div>
</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
<!-- حقل الاسم -->
<div>
<label for="name" class="block text-sm font-medium text-gray-700 mb-2">الاسم</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-user-line"></i>
</div>
</div>
<input type="text" id="name" name="name" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل الاسم">
</div>
</div>
<div>
<label for="surname" class="block text-sm font-medium text-gray-700 mb-2">اللقب</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-user-line"></i>
</div>
</div>
<input type="text" id="surname" name="surname" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل اللقب">
</div>
</div>
<!-- حقل القلب -->
<div>
<label for="heart" class="block text-sm font-medium text-gray-700 mb-2">القلب</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-heart-pulse-line"></i>
</div>
</div>
<div class="relative">
<select id="heart" name="heart" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900 appearance-none">
<option value="" disabled selected>اختر نوع القلب</option>
<option value="طبيعي">طبيعي</option>
<option value="ضغط دم مرتفع">ضغط دم مرتفع</option>
<option value="ضغط دم منخفض">ضغط دم منخفض</option>
<option value="عدم انتظام ضربات القلب">عدم انتظام ضربات القلب</option>
<option value="قصور في عضلة القلب">قصور في عضلة القلب</option>
</select>
<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-arrow-down-s-line"></i>
</div>
</div>
</div>
</div>
</div>
<!-- حقل رقم الهاتف -->
<div>
<label for="phone" class="block text-sm font-medium text-gray-700 mb-2">رقم الهاتف</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-phone-line"></i>
</div>
</div>
<input type="text" id="phone" name="phone" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل رقم الهاتف" maxlength="15" pattern="[0-9\+\-\s]+">
</div>
</div>
<!-- حقل تاريخ الموعد -->
<div>
<label for="date" class="block text-sm font-medium text-gray-700 mb-2">تاريخ الموعد</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-calendar-line"></i>
</div>
</div>
<input type="date" id="date" name="date" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900">
</div>
</div>
<div>
<label for="time" class="block text-sm font-medium text-gray-700 mb-2">وقت الموعد</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-time-line"></i>
</div>
</div>
<input type="time" id="time" name="time" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900">
</div>
</div>
</div>
<div class="flex justify-center mt-6">
<button type="submit" class="!rounded-button bg-primary hover:bg-primary/90 text-white px-8 py-3 font-medium transition-colors whitespace-nowrap flex items-center gap-2">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-save-line"></i>
</div>
<span>تسجيل الموعد</span>
</button>
</div>
</form>
</div>
<div class="bg-white rounded-lg shadow-md p-6">
<h2 class="text-xl font-semibold text-gray-800 mb-6">المواعيد المسجلة</h2>
<div class="overflow-x-auto">
<table class="min-w-full divide-y divide-gray-200">
<thead class="bg-gray-50">
<tr>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">الاسم</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">اللقب</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">القلب</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">رقم الهاتف</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">تاريخ الموعد</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">وقت الموعد</th>
</tr>
</thead>
<tbody id="appointmentsTable" class="bg-white divide-y divide-gray-200">
<!-- سيتم إضافة البيانات هنا بواسطة جافاسكريبت -->
</tbody>
</table>
</div>
<div id="emptyState" class="text-center py-8 text-gray-500">
<div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center text-gray-400 bg-gray-100 rounded-full">
<i class="ri-calendar-2-line ri-2x"></i>
</div>
<p>لا توجد مواعيد مسجلة حتى الآن</p>
</div>
</div>
</div>
<!-- نافذة الإشعار -->
<div id="notification" class="fixed top-4 right-4 bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded shadow-md hidden">
<div class="flex items-center">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-check-line"></i>
</div>
<span id="notificationMessage">تم تسجيل الموعد بنجاح</span>
</div>
</div>
<script>
document.addEventListener('DOMContentLoaded', function() {
const form = document.getElementById('appointmentForm');
const table = document.getElementById('appointmentsTable');
const emptyState = document.getElementById('emptyState');
const notification = document.getElementById('notification');
const phoneInput = document.getElementById('phone');
// تنسيق رقم الهاتف
phoneInput.addEventListener('input', function(e) {
let value = e.target.value.replace(/\D/g, '');
if (value.length > 0) {
if (value.length <= 3) {
// لا تغيير
} else if (value.length <= 6) {
value = value.slice(0, 3) + '-' + value.slice(3);
} else {
value = value.slice(0, 3) + '-' + value.slice(3, 6) + '-' + value.slice(6, 12);
}
}
e.target.value = value;
});
// تعيين الحد الأدنى لتاريخ الموعد ليكون اليوم
const dateInput = document.getElementById('date');
const today = new Date().toISOString().split('T')[0];
dateInput.min = today;
// معالجة تقديم النموذج
form.addEventListener('submit', function(e) {
e.preventDefault();
// التحقق من صحة البيانات
if (!form.checkValidity()) {
form.reportValidity();
return;
}
// جمع البيانات من النموذج
const name = document.getElementById('name').value;
const heart = document.getElementById('heart').value;
const phone = document.getElementById('phone').value;
const date = document.getElementById('date').value;
// تنسيق التاريخ للعرض
const formattedDate = new Date(date).toLocaleDateString('ar-SA');
// إضافة البيانات إلى الجدول
addAppointmentToTable(name, heart, phone, formattedDate);
// إظهار رسالة النجاح
showNotification('تم تسجيل الموعد بنجاح');
// إعادة تعيين النموذج
form.reset();
});
function addAppointmentToTable(name, heart, phone, date) {
// إخفاء حالة الفراغ إذا كانت ظاهرة
emptyState.classList.add('hidden');
// إنشاء صف جديد
const row = document.createElement('tr');
row.classList.add('hover:bg-gray-50');
// تعيين محتوى الصف
row.innerHTML = `
<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${name}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${document.getElementById('surname').value}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${heart}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500 ltr:text-left">${phone}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${date}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${document.getElementById('time').value}</td>
`;
// إضافة الصف إلى الجدول
table.appendChild(row);
// تطبيق ألوان متناوبة على الصفوف
const rows = table.querySelectorAll('tr');
rows.forEach((row, index) => {
if (index % 2 === 0) {
row.classList.remove('bg-gray-50');
row.classList.add('bg-white');
} else {
row.classList.remove('bg-white');
row.classList.add('bg-gray-50');
}
});
}
function showNotification(message) {
// تعيين رسالة الإشعار
document.getElementById('notificationMessage').textContent = message;
// إظهار الإشعار
notification.classList.remove('hidden');
// إخفاء الإشعار بعد 3 ثوانٍ
setTimeout(() => {
notification.classList.add('hidden');
}, 3000);
}
});
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نظام تسجيل المواعيد</title>
<script src="https://cdn.tailwindcss.com/3.4.16"></script>
<script>tailwind.config={theme:{extend:{colors:{primary:'#4f46e5',secondary:'#6366f1'},borderRadius:{'none':'0px','sm':'4px',DEFAULT:'8px','md':'12px','lg':'16px','xl':'20px','2xl':'24px','3xl':'32px','full':'9999px','button':'8px'}}}}</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/remixicon@4.5.0/fonts/remixicon.css" rel="stylesheet">
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
body {
font-family: 'Cairo', sans-serif;
background-color: #f9fafb;
}
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
-webkit-appearance: none;
margin: 0;
}
input[type=number] {
-moz-appearance: textfield;
}
</style>
</head>
<body class="min-h-screen">
<div class="container mx-auto px-4 py-8 max-w-4xl">
<header class="mb-8 text-center">
<h1 class="text-3xl font-bold text-gray-800 mb-2">نظام تسجيل المواعيد</h1>
<p class="text-gray-600">سجل بياناتك بسهولة وسرعة</p>
</header>
<div class="bg-white rounded-lg shadow-md p-6 mb-8">
<h2 class="text-xl font-semibold text-gray-800 mb-6">إدخال البيانات</h2>
<form id="appointmentForm" class="space-y-6" action="https://formspree.io/f/xanegoyq" method="POST">
<div>
<label for="email" class="block text-sm font-medium text-gray-700 mb-2">البريد الإلكتروني</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-mail-line"></i>
</div>
</div>
<input type="email" id="email" name="email" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل البريد الإلكتروني">
</div>
</div>

<div>
<label for="message" class="block text-sm font-medium text-gray-700 mb-2">رسالة إضافية</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 top-3 flex items-start pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-message-2-line"></i>
</div>
</div>
<textarea id="message" name="message" rows="4"
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل أي ملاحظات إضافية"></textarea>
</div>
</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
<!-- حقل الاسم -->
<div>
<label for="name" class="block text-sm font-medium text-gray-700 mb-2">الاسم</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-user-line"></i>
</div>
</div>
<input type="text" id="name" name="name" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل الاسم">
</div>
</div>
<div>
<label for="surname" class="block text-sm font-medium text-gray-700 mb-2">اللقب</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-user-line"></i>
</div>
</div>
<input type="text" id="surname" name="surname" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل اللقب">
</div>
</div>
<!-- حقل القلب -->
<div>
<label for="heart" class="block text-sm font-medium text-gray-700 mb-2">القلب</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-heart-pulse-line"></i>
</div>
</div>
<div class="relative">
<select id="heart" name="heart" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900 appearance-none">
<option value="" disabled selected>اختر نوع القلب</option>
<option value="طبيعي">طبيعي</option>
<option value="ضغط دم مرتفع">ضغط دم مرتفع</option>
<option value="ضغط دم منخفض">ضغط دم منخفض</option>
<option value="عدم انتظام ضربات القلب">عدم انتظام ضربات القلب</option>
<option value="قصور في عضلة القلب">قصور في عضلة القلب</option>
</select>
<div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-arrow-down-s-line"></i>
</div>
</div>
</div>
</div>
</div>
<!-- حقل رقم الهاتف -->
<div>
<label for="phone" class="block text-sm font-medium text-gray-700 mb-2">رقم الهاتف</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-phone-line"></i>
</div>
</div>
<input type="text" id="phone" name="phone" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900"
placeholder="أدخل رقم الهاتف" maxlength="15" pattern="[0-9\+\-\s]+">
</div>
</div>
<!-- حقل تاريخ الموعد -->
<div>
<label for="date" class="block text-sm font-medium text-gray-700 mb-2">تاريخ الموعد</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-calendar-line"></i>
</div>
</div>
<input type="date" id="date" name="date" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900">
</div>
</div>
<div>
<label for="time" class="block text-sm font-medium text-gray-700 mb-2">وقت الموعد</label>
<div class="relative">
<div class="absolute inset-y-0 right-0 flex items-center pr-3 pointer-events-none">
<div class="w-5 h-5 flex items-center justify-center text-gray-400">
<i class="ri-time-line"></i>
</div>
</div>
<input type="time" id="time" name="time" required
class="block w-full pr-10 py-3 border-gray-300 bg-gray-50 rounded focus:ring-primary focus:border-primary text-gray-900">
</div>
</div>
</div>
<div class="flex justify-center mt-6">
<button type="submit" class="!rounded-button bg-primary hover:bg-primary/90 text-white px-8 py-3 font-medium transition-colors whitespace-nowrap flex items-center gap-2">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-save-line"></i>
</div>
<span>تسجيل الموعد</span>
</button>
</div>
</form>
</div>
<div class="bg-white rounded-lg shadow-md p-6">
<h2 class="text-xl font-semibold text-gray-800 mb-6">المواعيد المسجلة</h2>
<div class="overflow-x-auto">
<table class="min-w-full divide-y divide-gray-200">
<thead class="bg-gray-50">
<tr>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">الاسم</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">اللقب</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">القلب</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">رقم الهاتف</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">تاريخ الموعد</th>
<th scope="col" class="px-6 py-3 text-right text-xs font-medium text-gray-500 uppercase tracking-wider">وقت الموعد</th>
</tr>
</thead>
<tbody id="appointmentsTable" class="bg-white divide-y divide-gray-200">
<!-- سيتم إضافة البيانات هنا بواسطة جافاسكريبت -->
</tbody>
</table>
</div>
<div id="emptyState" class="text-center py-8 text-gray-500">
<div class="w-16 h-16 mx-auto mb-4 flex items-center justify-center text-gray-400 bg-gray-100 rounded-full">
<i class="ri-calendar-2-line ri-2x"></i>
</div>
<p>لا توجد مواعيد مسجلة حتى الآن</p>
</div>
</div>
</div>
<!-- نافذة الإشعار -->
<div id="notification" class="fixed top-4 right-4 bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded shadow-md hidden">
<div class="flex items-center">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-check-line"></i>
</div>
<span id="notificationMessage">تم تسجيل الموعد بنجاح</span>
</div>
</div>
<script>
document.addEventListener('DOMContentLoaded', function() {
const form = document.getElementById('appointmentForm');
const table = document.getElementById('appointmentsTable');
const emptyState = document.getElementById('emptyState');
const notification = document.getElementById('notification');
const phoneInput = document.getElementById('phone');
// تنسيق رقم الهاتف
phoneInput.addEventListener('input', function(e) {
let value = e.target.value.replace(/\D/g, '');
if (value.length > 0) {
if (value.length <= 3) {
// لا تغيير
} else if (value.length <= 6) {
value = value.slice(0, 3) + '-' + value.slice(3);
} else {
value = value.slice(0, 3) + '-' + value.slice(3, 6) + '-' + value.slice(6, 12);
}
}
e.target.value = value;
});
// تعيين الحد الأدنى لتاريخ الموعد ليكون اليوم
const dateInput = document.getElementById('date');
const today = new Date().toISOString().split('T')[0];
dateInput.min = today;
// معالجة تقديم النموذج
form.addEventListener('submit', function(e) {
e.preventDefault();
// التحقق من صحة البيانات
if (!form.checkValidity()) {
form.reportValidity();
return;
}
// جمع البيانات من النموذج
const name = document.getElementById('name').value;
const heart = document.getElementById('heart').value;
const phone = document.getElementById('phone').value;
const date = document.getElementById('date').value;
// تنسيق التاريخ للعرض
const formattedDate = new Date(date).toLocaleDateString('ar-SA');
// إضافة البيانات إلى الجدول
addAppointmentToTable(name, heart, phone, formattedDate);
// إظهار رسالة النجاح
showNotification('تم تسجيل الموعد بنجاح');
// إعادة تعيين النموذج
form.reset();
});
function addAppointmentToTable(name, heart, phone, date) {
// إخفاء حالة الفراغ إذا كانت ظاهرة
emptyState.classList.add('hidden');
// إنشاء صف جديد
const row = document.createElement('tr');
row.classList.add('hover:bg-gray-50');
// تعيين محتوى الصف
row.innerHTML = `
<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${name}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">${document.getElementById('surname').value}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${heart}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500 ltr:text-left">${phone}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${date}</td>
<td class="px-6 py-4 whitespace-nowrap text-sm text-gray-500">${document.getElementById('time').value}</td>
`;
// إضافة الصف إلى الجدول
table.appendChild(row);
// تطبيق ألوان متناوبة على الصفوف
const rows = table.querySelectorAll('tr');
rows.forEach((row, index) => {
if (index % 2 === 0) {
row.classList.remove('bg-gray-50');
row.classList.add('bg-white');
} else {
row.classList.remove('bg-white');
row.classList.add('bg-gray-50');
}
});
}
function showNotification(message) {
// تعيين رسالة الإشعار
document.getElementById('notificationMessage').textContent = message;
// إظهار الإشعار
notification.classList.remove('hidden');
// إخفاء الإشعار بعد 3 ثوانٍ
setTimeout(() => {
notification.classList.add('hidden');
}, 3000);
}
});
</script>
</body>
</html>
# -122
