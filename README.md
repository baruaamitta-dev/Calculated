<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>মেমো ক্যালকুলেটর - কাজের সময় হিসাব</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            font-family: 'Segoe UI', 'SolaimanLipi', sans-serif;
            background: #f0f2f5;
            padding: 20px;
            color: #333;
        }
        .container {
            max-width: 700px;
            margin: 0 auto;
            background: white;
            border-radius: 16px;
            padding: 30px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #1a5276;
            margin-bottom: 5px;
            font-size: 26px;
        }
        .subtitle {
            text-align: center;
            color: #888;
            margin-bottom: 25px;
            font-size: 14px;
        }
        .form-row {
            display: flex;
            gap: 12px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }
        .form-group {
            flex: 1;
            min-width: 140px;
        }
        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
            color: #555;
            font-size: 14px;
        }
        input, select {
            width: 100%;
            padding: 10px 12px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 15px;
            transition: border-color 0.2s;
        }
        input:focus, select:focus {
            outline: none;
            border-color: #1a5276;
        }
        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 10px;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }
        .btn-primary {
            background: #1a5276;
            color: white;
            width: 100%;
            margin-top: 10px;
        }
        .btn-primary:hover { background: #154360; }
        .btn-danger {
            background: #e74c3c;
            color: white;
            padding: 8px 16px;
            font-size: 13px;
        }
        .btn-danger:hover { background: #c0392b; }
        .btn-export {
            background: #27ae60;
            color: white;
            padding: 10px 20px;
            font-size: 14px;
            margin-top: 15px;
        }
        .btn-export:hover { background: #1e8449; }
        .btn-clear {
            background: #f39c12;
            color: white;
            padding: 10px 20px;
            font-size: 14px;
            margin-top: 15px;
            margin-left: 10px;
        }
        .btn-clear:hover { background: #d68910; }

        .summary {
            background: #eaf2f8;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
            text-align: center;
        }
        .summary h3 {
            color: #1a5276;
            margin-bottom: 10px;
        }
        .summary .total {
            font-size: 36px;
            font-weight: 700;
            color: #1a5276;
        }
        .summary .total-label {
            font-size: 14px;
            color: #666;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 14px;
        }
        th {
            background: #1a5276;
            color: white;
            padding: 12px;
            text-align: left;
        }
        td {
            padding: 12px;
            border-bottom: 1px solid #eee;
        }
        tr:hover { background: #f8f9fa; }
        .hours-cell {
            font-weight: 600;
            color: #1a5276;
        }
        .empty-msg {
            text-align: center;
            color: #999;
            padding: 30px;
            font-style: italic;
        }
        .actions {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .date-group {
            background: #f8f9fa;
            border-radius: 8px;
            padding: 8px 12px;
            margin-bottom: 8px;
            font-weight: 600;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>📝 মেমো ক্যালকুলেটর</h1>
        <p class="subtitle">কাজের সময় হিসাব করুন</p>

        <div class="form-row">
            <div class="form-group">
                <label for="date">📅 তারিখ</label>
                <input type="date" id="date">
            </div>
            <div class="form-group">
                <label for="task">📝 কাজের বিবরণ</label>
                <input type="text" id="task" placeholder="যেমন: ওয়েবসাইট ডিজাইন">
            </div>
        </div>

        <div class="form-row">
            <div class="form-group">
                <label for="st
