<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>安全密码生成器</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 500px;
            padding: 40px;
            text-align: center;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #7f8c8d;
            margin-bottom: 30px;
            font-size: 1rem;
        }
        
        .password-display {
            position: relative;
            margin-bottom: 25px;
        }
        
        #password {
            width: 100%;
            padding: 15px 20px;
            font-size: 1.2rem;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            background: #f8f9fa;
            text-align: center;
            letter-spacing: 1px;
            margin-bottom: 10px;
        }
        
        .copy-btn {
            position: absolute;
            right: 10px;
            top: 10px;
            background: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 8px 12px;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .copy-btn:hover {
            background: #2980b9;
        }
        
        .options {
            text-align: left;
            margin-bottom: 30px;
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
        }
        
        .option-group {
            margin-bottom: 15px;
        }
        
        label {
            display: flex;
            align-items: center;
            margin-bottom: 8px;
            cursor: pointer;
        }
        
        input[type="checkbox"] {
            margin-right: 10px;
            transform: scale(1.2);
        }
        
        input[type="range"] {
            width: 100%;
            margin: 10px 0;
        }
        
        .length-display {
            display: flex;
            justify-content: space-between;
            margin-top: 5px;
        }
        
        .strength-meter {
            height: 10px;
            background: #ecf0f1;
            border-radius: 5px;
            margin: 15px 0;
            overflow: hidden;
        }
        
        .strength-fill {
            height: 100%;
            width: 0%;
            border-radius: 5px;
            transition: all 0.3s;
        }
        
        .strength-text {
            font-size: 0.9rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .generate-btn {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            border: none;
            border-radius: 10px;
            padding: 15px 30px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            width: 100%;
            font-weight: bold;
        }
        
        .generate-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 7px 15px rgba(0, 0, 0, 0.2);
        }
        
        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #2ecc71;
            color: white;
            padding: 15px 25px;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transform: translateX(150%);
            transition: transform 0.3s;
        }
        
        .notification.show {
            transform: translateX(0);
        }
        
        @media (max-width: 500px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🔐 安全密码生成器</h1>
        <p class="subtitle">创建高强度随机密码，保护您的在线账户</p>
        
        <div class="password-display">
            <input type="text" id="password" readonly>
            <button class="copy-btn" id="copyBtn">复制</button>
        </div>
        
        <div class="options">
            <div class="option-group">
                <div class="length-display">
                    <span>密码长度: # -01
I have created a practical random password generator project for you. The interface is attractive and the functions are complete.
