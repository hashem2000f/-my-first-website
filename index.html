<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مدير الإشارات المرجعية</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
  <style>
    html, body {
      height: 100%;
      margin: 0;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }

    /* تحديد الألوان حسب نوع الجهاز */
    /* اللون الافتراضي */
    body {
      background-color: #f8f9fa; /* اللون العام */
    }

    /* لأجهزة الكمبيوتر المحمول */
    @media (min-width: 1025px) {
      body {
        background-color: #e9ecef; /* لون خاص للكمبيوتر المحمول */
      }
      .card {
        border: 2px solid #343a40;
      }
    }

    /* لأجهزة التابلت */
    @media (max-width: 1024px) and (min-width: 576px) {
      body {
        background-color: #d1ecf1; /* لون خاص للآيباد */
      }
      .card {
        border: 2px solid #007bff;
      }
    }

    /* لأجهزة الهاتف المحمول */
    @media (max-width: 575px) {
      body {
        background-color: #f1c40f; /* لون خاص للهاتف المحمول */
      }
      .card {
        border: 2px solid #ff8c00;
      }
    }

    /* تكبير الـ card وتنسيق النصوص */
    .container-fixed {
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 1rem;
    }

    .card {
      width: 100%;
      max-width: 800px;
      height: 100%;
      background-color: #ffffff;
      border-radius: 15px;
      padding: 1.5rem;
      display: flex;
      flex-direction: column;
    }

    .form-section {
      flex-shrink: 0;
    }

    #bookmarkItems {
      max-height: 250px;
      overflow-y: auto;
      margin-top: 1rem;
    }

    .list-group-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .bookmark-text {
      flex: 1;
      overflow-x: auto;
      white-space: nowrap;
      text-overflow: ellipsis;
    }

    /* تظليل النص باللون الأخضر عند التمرير */
    .bookmark-text a {
      text-decoration: none;
      color: inherit;
      transition: color 0.3s ease, text-decoration 0.3s ease;
    }

    .bookmark-text a:hover {
      color: green; /* تغيير اللون إلى الأخضر عند التمرير */
      text-decoration: none; /* إزالة الخط تحت الرابط */
    }

    .bookmark-actions {
      flex-shrink: 0;
      display: flex;
      gap: 0.5rem;
    }

    /* تحسين الشكل في الشاشات الصغيرة */
    @media (max-width: 576px) {
      .card {
        padding: 1rem;
      }
      
      .list-group-item {
        flex-direction: column;
        align-items: flex-start;
      }

      .bookmark-actions {
        margin-top: 0.5rem;
      }
    }

    /* تحسين عرض الفورم في الشاشات الصغيرة */
    @media (max-width: 576px) {
      #bookmarkForm input {
        width: 100%;
        margin-bottom: 1rem;
      }
    }
  </style>
</head>
<body>
  <div class="container-fixed">
    <h1 class="text-center text-primary fw-bold mb-3">📌 مدير الإشارات المرجعية</h1>
    <div class="card shadow-sm">
      <div class="form-section">
        <form id="bookmarkForm" class="mb-3">
          <div class="row g-3">
            <div class="col-12 col-md-6">
              <input type="text" id="siteName" class="form-control" placeholder="اسم الموقع" required>
            </div>
            <div class="col-12 col-md-6">
              <input type="url" id="siteURL" class="form-control" placeholder="رابط الموقع" required>
            </div>
          </div>
          <button type="submit" id="submitButton" class="btn btn-primary mt-3 w-100">أضف الإشارة المرجعية</button>
        </form>
        <input type="text" id="searchInput" class="form-control mb-3" placeholder="ابحث في الإشارات..." onkeyup="searchBookmarks()">
      </div>
      <div class="flex-grow-1 d-flex flex-column">
        <h5>إشاراتك المرجعية:</h5>
        <ul class="list-group flex-grow-1 overflow-auto" id="bookmarkItems">
          <!-- bookmarks will appear here -->
        </ul>
      </div>
    </div>
  </div>

  <script>
    let editIndex = -1;
    let isEditing = false;

    function loadBookmarks() {
      const bookmarks = JSON.parse(localStorage.getItem('bookmarks')) || [];
      const bookmarkItems = document.getElementById('bookmarkItems');
      bookmarkItems.innerHTML = '';

      bookmarks.forEach((bookmark, index) => {
        const li = document.createElement('li');
        li.className = 'list-group-item';
        li.innerHTML = `
          <div class="bookmark-text">
            <a href="${bookmark.url}" target="_blank">${bookmark.name}</a>
          </div>
          <div class="bookmark-actions">
            <button class="btn btn-warning btn-sm" onclick="editBookmark(${index})">
              <i class="fas fa-edit"></i> تعديل
            </button>
            <button class="btn btn-danger btn-sm" onclick="deleteBookmark(${index})">
              <i class="fas fa-trash"></i> حذف
            </button>
          </div>
        `;
        bookmarkItems.appendChild(li);
      });
    }

    function saveBookmarks(bookmarks) {
      localStorage.setItem('bookmarks', JSON.stringify(bookmarks));
    }

    function editBookmark(index) {
      const bookmarks = JSON.parse(localStorage.getItem('bookmarks')) || [];
      const bookmark = bookmarks[index];
      document.getElementById('siteName').value = bookmark.name;
      document.getElementById('siteURL').value = bookmark.url;
      editIndex = index;
      isEditing = true;
      document.getElementById('submitButton').textContent = 'حفظ التعديل';
    }

    function deleteBookmark(index) {
      const bookmarks = JSON.parse(localStorage.getItem('bookmarks')) || [];
      if (confirm("هل تريد حذف هذه الإشارة المرجعية؟")) {
        bookmarks.splice(index, 1);
        saveBookmarks(bookmarks);
        loadBookmarks();
      }
    }

    document.getElementById('bookmarkForm').addEventListener('submit', function (e) {
      e.preventDefault();
      const name = document.getElementById('siteName').value.trim();
      const url = document.getElementById('siteURL').value.trim();

      if (!name || !url) {
        alert("الرجاء ملء الحقول");
        return;
      }

      const bookmarks = JSON.parse(localStorage.getItem('bookmarks')) || [];

      if (isEditing) {
        bookmarks[editIndex] = { name, url };
        isEditing = false;
        editIndex = -1;
        document.getElementById('submitButton').textContent = 'أضف الإشارة المرجعية';
      } else {
        const exists = bookmarks.some(b => b.url === url);
        if (exists) {
          alert("هذا الرابط موجود بالفعل.");
          return;
        }
        bookmarks.push({ name, url });
      }

      saveBookmarks(bookmarks);
      this.reset();
      loadBookmarks();
    });

    function searchBookmarks() {
      const search = document.getElementById('searchInput').value.toLowerCase();
      const bookmarks = JSON.parse(localStorage.getItem('bookmarks')) || [];
      const bookmarkItems = document.getElementById('bookmarkItems');
      bookmarkItems.innerHTML = '';

      bookmarks.forEach((bookmark, index) => {
        if (bookmark.name.toLowerCase().includes(search)) {
          const li = document.createElement('li');
          li.className = 'list-group-item';
          li.innerHTML = `
            <div class="bookmark-text">
              <a href="${bookmark.url}" target="_blank">${bookmark.name}</a>
            </div>
            <div class="bookmark-actions">
              <button class="btn btn-warning btn-sm" onclick="editBookmark(${index})">
                <i class="fas fa-edit"></i> تعديل
              </button>
              <button class="btn btn-danger btn-sm" onclick="deleteBookmark(${index})">
                <i class="fas fa-trash"></i> حذف
              </button>
            </div>
          `;
          bookmarkItems.appendChild(li);
        }
      });
    }

    // تحميل الإشارات عند فتح الصفحة
    loadBookmarks();
  </script>
</body>
</html>
