<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>أنواع العضوية | SFMS Membership Types</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Naskh+Arabic:wght@400;500;600;700&family=Cormorant+Garamond:wght@400;600;700&family=Source+Serif+4:ital,wght@0,300;0,400;0,600;1,400&display=swap" rel="stylesheet">
  <style>
    :root {
      --teal:        #1A6B6B;
      --teal-mid:    #22878A;
      --teal-light:  #2FA8AB;
      --teal-pale:   #E6F4F4;
      --teal-faint:  #F2FAFA;
      --gold:        #C5973A;
      --gold-pale:   #FBF3E2;
      --dark:        #162424;
      --mid:         #3D5C5C;
      --muted:       #7A9898;
      --line:        #D0E6E6;
      --bg:          #F5FAFA;
      --white:       #FFFFFF;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      font-family: 'Noto Naskh Arabic', 'Source Serif 4', Georgia, serif;
      color: var(--dark);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── HERO HEADER ── */
    .hero {
      background: var(--dark);
      position: relative;
      overflow: hidden;
      padding: 64px 40px 56px;
      text-align: center;
    }
    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        radial-gradient(ellipse 80% 60% at 50% 110%, rgba(26,107,107,0.55) 0%, transparent 70%),
        radial-gradient(ellipse 40% 40% at 10% 20%, rgba(197,151,58,0.12) 0%, transparent 60%);
    }
    /* Geometric pattern overlay */
    .hero::after {
      content: '';
      position: absolute;
      inset: 0;
      background-image: repeating-linear-gradient(
        45deg,
        rgba(255,255,255,0.015) 0px,
        rgba(255,255,255,0.015) 1px,
        transparent 1px,
        transparent 28px
      ),
      repeating-linear-gradient(
        -45deg,
        rgba(255,255,255,0.015) 0px,
        rgba(255,255,255,0.015) 1px,
        transparent 1px,
        transparent 28px
      );
    }
    .hero-inner {
      position: relative;
      z-index: 1;
      max-width: 800px;
      margin: 0 auto;
    }
    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(197,151,58,0.15);
      border: 1px solid rgba(197,151,58,0.4);
      color: #E4BE72;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 1px;
      padding: 5px 16px;
      border-radius: 20px;
      margin-bottom: 22px;
      font-family: 'Source Serif 4', serif;
      text-transform: uppercase;
      direction: ltr;
    }
    .hero-title-ar {
      font-family: 'Noto Naskh Arabic', serif;
      font-size: clamp(26px, 4vw, 40px);
      font-weight: 700;
      color: var(--white);
      line-height: 1.3;
      margin-bottom: 8px;
    }
    .hero-title-en {
      font-family: 'Cormorant Garamond', Georgia, serif;
      font-size: clamp(15px, 2.5vw, 22px);
      font-weight: 400;
      color: rgba(255,255,255,0.6);
      font-style: italic;
      margin-bottom: 20px;
      direction: ltr;
    }
    .hero-divider {
      width: 60px;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      margin: 20px auto;
    }
    .hero-desc {
      font-size: 15px;
      color: rgba(255,255,255,0.72);
      line-height: 1.85;
      max-width: 580px;
      margin: 0 auto;
    }

    /* ── MAIN CONTENT ── */
    .page-body {
      max-width: 1020px;
      margin: 0 auto;
      padding: 52px 24px 72px;
    }

    /* ── SECTION LABEL ── */
    .section-label {
      text-align: center;
      margin-bottom: 36px;
    }
    .section-label h2 {
      font-family: 'Noto Naskh Arabic', serif;
      font-size: 22px;
      font-weight: 700;
      color: var(--teal);
      margin-bottom: 4px;
    }
    .section-label p {
      font-family: 'Source Serif 4', serif;
      font-size: 13px;
      color: var(--muted);
      direction: ltr;
    }

    /* ── CARDS GRID ── */
    .cards-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 28px;
    }

    /* ── MEMBERSHIP CARD ── */
    .mem-card {
      background: var(--white);
      border-radius: 16px;
      border: 1px solid var(--line);
      overflow: hidden;
      box-shadow: 0 4px 24px rgba(22,36,36,0.06);
      display: flex;
      flex-direction: column;
      transition: transform .3s, box-shadow .3s;
      animation: fadeUp .6s ease both;
    }
    .mem-card:nth-child(2) { animation-delay: .15s; }
    .mem-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 40px rgba(26,107,107,0.13);
    }
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* Card header */
    .card-header {
      padding: 32px 28px 24px;
      position: relative;
      overflow: hidden;
    }
    .card-header::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--line), transparent);
    }
    .card--regular .card-header {
      background: linear-gradient(135deg, #0F3F3F 0%, var(--teal) 100%);
    }
    .card--student .card-header {
      background: linear-gradient(135deg, #3B2800 0%, #8B5E1A 60%, var(--gold) 100%);
    }

    .card-icon-wrap {
      width: 52px; height: 52px;
      border-radius: 14px;
      background: rgba(255,255,255,0.15);
      border: 1px solid rgba(255,255,255,0.25);
      display: flex; align-items: center; justify-content: center;
      font-size: 22px;
      margin-bottom: 16px;
      backdrop-filter: blur(4px);
    }
    .card-type-tag {
      display: inline-block;
      font-family: 'Source Serif 4', serif;
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: rgba(255,255,255,0.65);
      background: rgba(255,255,255,0.1);
      border: 1px solid rgba(255,255,255,0.2);
      padding: 3px 10px;
      border-radius: 10px;
      margin-bottom: 8px;
      direction: ltr;
    }
    .card-title-ar {
      font-family: 'Noto Naskh Arabic', serif;
      font-size: 22px;
      font-weight: 700;
      color: var(--white);
      display: block;
      margin-bottom: 2px;
    }
    .card-title-en {
      font-family: 'Cormorant Garamond', serif;
      font-size: 14px;
      color: rgba(255,255,255,0.6);
      font-style: italic;
      direction: ltr;
      display: block;
    }

    /* Card body */
    .card-body {
      padding: 28px;
      flex: 1;
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

    /* Block: eligibility / benefits */
    .info-block {}
    .info-block-title {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 13px;
      font-weight: 700;
      color: var(--mid);
      margin-bottom: 14px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      direction: rtl;
    }
    .info-block-title .dot {
      width: 8px; height: 8px;
      border-radius: 50%;
      flex-shrink: 0;
    }
    .card--regular .info-block-title .dot { background: var(--teal); }
    .card--student .info-block-title .dot { background: var(--gold); }

    .info-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .info-list li {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      font-size: 14px;
      line-height: 1.7;
      color: var(--mid);
      direction: rtl;
    }
    .info-list li .ic {
      flex-shrink: 0;
      margin-top: 3px;
      font-size: 14px;
    }
    .card--regular .info-list li .ic { color: var(--teal-light); }
    .card--student .info-list li .ic { color: var(--gold); }

    /* Divider inside card */
    .card-rule {
      height: 1px;
      background: var(--line);
    }

    /* CTA button */
    .card-cta {
      margin-top: auto;
    }
    .btn-apply {
      display: block;
      width: 100%;
      padding: 13px 20px;
      border: none;
      border-radius: 10px;
      font-family: 'Noto Naskh Arabic', serif;
      font-size: 15px;
      font-weight: 700;
      cursor: pointer;
      transition: all .25s;
      text-align: center;
      text-decoration: none;
    }
    .card--regular .btn-apply {
      background: linear-gradient(135deg, var(--teal), var(--teal-light));
      color: white;
      box-shadow: 0 4px 18px rgba(26,107,107,0.28);
    }
    .card--regular .btn-apply:hover {
      box-shadow: 0 8px 28px rgba(26,107,107,0.4);
      transform: translateY(-1px);
    }
    .card--student .btn-apply {
      background: linear-gradient(135deg, #8B5E1A, var(--gold));
      color: white;
      box-shadow: 0 4px 18px rgba(197,151,58,0.28);
    }
    .card--student .btn-apply:hover {
      box-shadow: 0 8px 28px rgba(197,151,58,0.4);
      transform: translateY(-1px);
    }
    .btn-apply span { display: block; font-size: 11px; opacity: 0.8; font-weight: 400; margin-top: 2px; direction: ltr; font-family: 'Source Serif 4', serif; }

    /* ── COMPARISON STRIP ── */
    .compare-strip {
      margin-top: 44px;
      background: var(--white);
      border: 1px solid var(--line);
      border-radius: 14px;
      overflow: hidden;
      box-shadow: 0 2px 12px rgba(22,36,36,0.05);
      animation: fadeUp .6s .3s ease both;
    }
    .compare-head {
      background: linear-gradient(90deg, var(--teal-faint), var(--white));
      padding: 16px 24px;
      display: flex;
      align-items: center;
      gap: 10px;
      border-bottom: 1px solid var(--line);
      direction: rtl;
    }
    .compare-head-title {
      font-size: 15px;
      font-weight: 700;
      color: var(--teal);
    }
    .compare-head-sub {
      font-size: 12px;
      color: var(--muted);
      font-family: 'Source Serif 4', serif;
      direction: ltr;
    }
    table.compare-table {
      width: 100%;
      border-collapse: collapse;
      direction: rtl;
      font-size: 13.5px;
    }
    .compare-table thead th {
      padding: 14px 20px;
      font-weight: 700;
      font-size: 13px;
      color: var(--mid);
      border-bottom: 1px solid var(--line);
      background: var(--teal-faint);
    }
    .compare-table thead th:first-child { text-align: right; }
    .compare-table thead th:not(:first-child) { text-align: center; width: 130px; }
    .compare-table tbody tr { border-bottom: 1px solid var(--line); }
    .compare-table tbody tr:last-child { border-bottom: none; }
    .compare-table tbody tr:hover { background: var(--teal-faint); }
    .compare-table td { padding: 12px 20px; color: var(--mid); }
    .compare-table td:first-child { font-weight: 500; }
    .compare-table td:not(:first-child) { text-align: center; }
    .check { color: var(--teal-light); font-size: 17px; }
    .check-gold { color: var(--gold); font-size: 17px; }
    .cross { color: #C0C8C8; font-size: 15px; }

    /* ── NOTE BOX ── */
    .note-box {
      margin-top: 28px;
      background: var(--gold-pale);
      border: 1px solid rgba(197,151,58,0.3);
      border-right: 4px solid var(--gold);
      border-radius: 10px;
      padding: 16px 20px;
      font-size: 13px;
      color: #6B4A10;
      line-height: 1.8;
      direction: rtl;
      animation: fadeUp .6s .45s ease both;
    }
    .note-box strong { font-weight: 700; }

    /* ── FOOTER NAV ── */
    .page-footer {
      text-align: center;
      padding: 28px 20px 48px;
      border-top: 1px solid var(--line);
      margin-top: 16px;
    }
    .footer-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--teal);
      font-size: 14px;
      font-weight: 600;
      text-decoration: none;
      padding: 10px 24px;
      border: 1.5px solid var(--teal);
      border-radius: 8px;
      transition: all .2s;
    }
    .footer-link:hover { background: var(--teal); color: white; }

    @media (max-width: 660px) {
      .cards-grid { grid-template-columns: 1fr; }
      .hero { padding: 44px 20px 40px; }
      .page-body { padding: 36px 16px 52px; }
      .compare-table td, .compare-table th { padding: 10px 12px; font-size: 12px; }
    }
  </style>
</head>
<body>

<!-- ── HERO ── -->
<div class="hero">
  <div class="hero-inner">
    <div class="hero-badge">🏥 SFMS · الجمعية السعودية</div>
    <div class="hero-title-ar">أنواع العضوية</div>
    <div class="hero-title-en">Membership Types</div>
    <div class="hero-divider"></div>
    <p class="hero-desc">
      تُرحّب الجمعية السعودية لتقييم الأدوية وإدارة القوائم العلاجية بانضمام المتخصصين والطلاب الراغبين في الإسهام في تطوير منظومة إدارة الدواء في المملكة.
    </p>
  </div>
</div>

<!-- ── BODY ── -->
<div class="page-body">

  <div class="section-label">
    <h2>اختر نوع العضوية المناسب</h2>
    <p>Choose the membership type that fits your profile</p>
  </div>

  <div class="cards-grid">

    <!-- ── REGULAR MEMBER ── -->
    <div class="mem-card card--regular">
      <div class="card-header">
        <div class="card-icon-wrap">🎓</div>
        <div class="card-type-tag">Regular Member</div>
        <span class="card-title-ar">العضو العادي</span>
        <span class="card-title-en">Regular Membership</span>
      </div>
      <div class="card-body">

        <!-- Eligibility -->
        <div class="info-block">
          <div class="info-block-title">
            <div class="dot"></div>
            شروط الأهلية &nbsp;·&nbsp; <span style="font-family:'Source Serif 4',serif;font-size:11px;font-weight:400;direction:ltr">Eligibility</span>
          </div>
          <ul class="info-list">
            <li><span class="ic">◈</span>حاصل على مؤهل علمي معتمد في أحد التخصصات الصحية أو الصيدلانية أو العلمية ذات الصلة</li>
            <li><span class="ic">◈</span>يعمل أو سبق له العمل في مجال تقييم الأدوية أو إدارة القوائم العلاجية أو المجالات المرتبطة بها</li>
            <li><span class="ic">◈</span>ملتزم بمبادئ وأخلاقيات الممارسة المهنية</li>
            <li><span class="ic">◈</span>مقيم في المملكة العربية السعودية أو مرتبط بمنظومتها الصحية</li>
          </ul>
        </div>

        <div class="card-rule"></div>

        <!-- Benefits -->
        <div class="info-block">
          <div class="info-block-title">
            <div class="dot"></div>
            مزايا العضوية &nbsp;·&nbsp; <span style="font-family:'Source Serif 4',serif;font-size:11px;font-weight:400;direction:ltr">Benefits</span>
          </div>
          <ul class="info-list">
            <li><span class="ic">✦</span>حق التصويت والترشح في انتخابات مجلس الإدارة</li>
            <li><span class="ic">✦</span>المشاركة الكاملة في اللجان العلمية وفرق العمل</li>
            <li><span class="ic">✦</span>الاطلاع على الدوريات والتقارير والمنشورات العلمية للجمعية</li>
            <li><span class="ic">✦</span>حضور المؤتمرات والورش بأسعار مخفضة أو مجاناً</li>
            <li><span class="ic">✦</span>الوصول إلى شبكة المتخصصين وفرص التواصل المهني</li>
            <li><span class="ic">✦</span>الأولوية في برامج التدريب والتطوير المهني</li>
            <li><span class="ic">✦</span>شهادة عضوية معتمدة من الجمعية</li>
          </ul>
        </div>

        <div class="card-cta">
          <a href="#" class="btn-apply">
            تقديم طلب العضوية العادية
            <span>Apply for Regular Membership</span>
          </a>
        </div>

      </div>
    </div>

    <!-- ── STUDENT MEMBER ── -->
    <div class="mem-card card--student">
      <div class="card-header">
        <div class="card-icon-wrap">📚</div>
        <div class="card-type-tag">Student Member</div>
        <span class="card-title-ar">العضو الطالب</span>
        <span class="card-title-en">Student Membership</span>
      </div>
      <div class="card-body">

        <!-- Eligibility -->
        <div class="info-block">
          <div class="info-block-title">
            <div class="dot"></div>
            شروط الأهلية &nbsp;·&nbsp; <span style="font-family:'Source Serif 4',serif;font-size:11px;font-weight:400;direction:ltr">Eligibility</span>
          </div>
          <ul class="info-list">
            <li><span class="ic">◈</span>مقيد حالياً في برنامج أكاديمي معتمد في الصيدلة أو الطب أو العلوم الصحية أو المجالات ذات الصلة</li>
            <li><span class="ic">◈</span>يحمل وثيقة إثبات قيد سارية من مؤسسته التعليمية</li>
            <li><span class="ic">◈</span>في مرحلة البكالوريوس أو الدراسات العليا (ماجستير / دكتوراه)</li>
            <li><span class="ic">◈</span>ملتزم بالسياسات والأخلاقيات المهنية للجمعية</li>
          </ul>
        </div>

        <div class="card-rule"></div>

        <!-- Benefits -->
        <div class="info-block">
          <div class="info-block-title">
            <div class="dot"></div>
            مزايا العضوية &nbsp;·&nbsp; <span style="font-family:'Source Serif 4',serif;font-size:11px;font-weight:400;direction:ltr">Benefits</span>
          </div>
          <ul class="info-list">
            <li><span class="ic">✦</span>حضور المؤتمرات والفعاليات العلمية بأسعار الطلاب المخفضة</li>
            <li><span class="ic">✦</span>الاطلاع على المنشورات والموارد التعليمية للجمعية</li>
            <li><span class="ic">✦</span>فرص التدريب والتوجيه من خبراء الجمعية</li>
            <li><span class="ic">✦</span>المشاركة في فرق الأبحاث والمشاريع الطلابية</li>
            <li><span class="ic">✦</span>بناء شبكة مهنية مبكرة مع المتخصصين في المجال</li>
            <li><span class="ic">✦</span>شهادة عضوية طلابية معتمدة قابلة للتحويل إلى عضوية عادية عند التخرج</li>
          </ul>
        </div>

        <div class="card-cta">
          <a href="#" class="btn-apply">
            تقديم طلب العضوية الطلابية
            <span>Apply for Student Membership</span>
          </a>
        </div>

      </div>
    </div>

  </div><!-- /cards-grid -->

  <!-- ── COMPARISON TABLE ── -->
  <div class="compare-strip">
    <div class="compare-head">
      <span style="font-size:18px">⚖️</span>
      <div>
        <div class="compare-head-title">مقارنة المزايا</div>
        <div class="compare-head-sub">Benefits Comparison</div>
      </div>
    </div>
    <table class="compare-table">
      <thead>
        <tr>
          <th>الميزة / Benefit</th>
          <th>عضو عادي<br><span style="font-weight:400;font-size:11px;direction:ltr">Regular</span></th>
          <th>عضو طالب<br><span style="font-weight:400;font-size:11px;direction:ltr">Student</span></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>حق التصويت والترشح — Voting & candidacy rights</td>
          <td><span class="check">✔</span></td>
          <td><span class="cross">—</span></td>
        </tr>
        <tr>
          <td>المشاركة في اللجان العلمية — Scientific committees</td>
          <td><span class="check">✔</span></td>
          <td><span class="cross">—</span></td>
        </tr>
        <tr>
          <td>المنشورات والتقارير العلمية — Publications & reports</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
        <tr>
          <td>حضور المؤتمرات بسعر مخفض — Discounted conference access</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
        <tr>
          <td>التدريب والتوجيه المهني — Training & mentorship</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
        <tr>
          <td>فرق الأبحاث — Research teams</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
        <tr>
          <td>شبكة التواصل المهني — Professional network</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
        <tr>
          <td>شهادة عضوية معتمدة — Accredited membership certificate</td>
          <td><span class="check">✔</span></td>
          <td><span class="check-gold">✔</span></td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- ── NOTE ── -->
  <div class="note-box">
    <strong>ملاحظة:</strong> تُحوَّل العضوية الطلابية تلقائياً إلى عضوية عادية عند التقديم بعد التخرج وتقديم وثائق المؤهل. لمزيد من المعلومات، يمكن التواصل مع الجمعية عبر البريد الإلكتروني الرسمي.
    <br>
    <span style="font-family:'Source Serif 4',serif;font-size:12px;direction:ltr;display:block;margin-top:6px;color:#8B6020;">
      <strong>Note:</strong> Student membership automatically upgrades to Regular membership upon graduation. Contact the Society for further details.
    </span>
  </div>

</div><!-- /page-body -->

<!-- ── FOOTER ── -->
<div class="page-footer">
  <a href="#" class="footer-link">
    ← العودة إلى صفحة العضوية &nbsp;|&nbsp; Back to Membership
  </a>
</div>

</body>
</html># sfms-membership-form
