<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LUXE Home AI Advisor | Premium Home Improvement Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2a5a78;
            --primary-light: #3a7ca5;
            --secondary: #d4a762;
            --dark: #1a2a3a;
            --light: #f8f9fa;
            --success: #5cb85c;
            --gray: #6c757d;
            --light-gray: #e9ecef;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Helvetica Neue', sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: var(--dark);
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            margin: 0 auto;
            padding: 20px;
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        /* Premium Header */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            padding: 2rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
            text-align: center;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            transform: rotate(30deg);
        }

        .header-content {
            position: relative;
            z-index: 2;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 1.5rem;
        }

        .badge {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--dark);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 15px rgba(212, 167, 98, 0.3);
        }

        /* Main Content Grid */
        .app-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
            margin-bottom: 2rem;
            flex: 1;
        }

        /* Form Section */
        .home-form {
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: var(--shadow);
            height: fit-content;
            margin: 0 auto;
            max-width: 800px;
            width: 100%;
            text-align: center;
        }

        .form-title {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            justify-content: center;
        }

        .form-title i {
            color: var(--secondary);
        }

        .form-group {
            margin-bottom: 1.5rem;
            text-align: center;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--primary);
            font-size: 0.95rem;
        }

        .form-control {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-size: 1rem;
            transition: var(--transition);
            background-color: var(--light);
            max-width: 600px;
            margin: 0 auto;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary-light);
            box-shadow: 0 0 0 3px rgba(42, 90, 120, 0.1);
        }

        textarea.form-control {
            min-height: 100px;
            resize: vertical;
        }

        /* Option Selectors */
        .option-group {
            margin-top: 0.5rem;
            display: flex;
            justify-content: center;
        }

        .option-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 0.75rem;
            max-width: 600px;
            width: 100%;
        }

        .option-btn {
            background-color: var(--light);
            border: 1px solid var(--light-gray);
            padding: 0.75rem;
            border-radius: 8px;
            cursor: pointer;
            text-align: center;
            font-size: 0.9rem;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
        }

        .option-btn i {
            font-size: 1.2rem;
            color: var(--primary);
        }

        .option-btn:hover {
            border-color: var(--primary-light);
        }

        .option-btn.selected {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .option-btn.selected i {
            color: white;
        }

        .budget-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            gap: 0.75rem;
            max-width: 600px;
            width: 100%;
        }

        /* File Upload */
        .upload-container {
            border: 2px dashed var(--light-gray);
            border-radius: 8px;
            padding: 1.5rem;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            margin-top: 0.5rem;
            max-width: 600px;
            margin: 0.5rem auto 0;
        }

        .upload-container:hover {
            border-color: var(--primary-light);
            background-color: rgba(58, 124, 165, 0.05);
        }

        .upload-icon {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .upload-text {
            font-size: 0.9rem;
            color: var(--gray);
            margin-bottom: 0.5rem;
        }

        .file-name {
            font-size: 0.85rem;
            color: var(--gray);
            margin-top: 0.5rem;
        }

        #image-upload {
            display: none;
        }

        /* Submit Button */
        .submit-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            border: none;
            border-radius: 8px;
            padding: 1rem;
            width: 100%;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(42, 90, 120, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(42, 90, 120, 0.4);
        }

        .submit-btn:active {
            transform: translateY(0);
        }

        /* Chat Container - Enhanced for Responsiveness */
        .chat-container {
            background-color: white;
            border-radius: 12px;
            box-shadow: var(--shadow);
            display: flex;
            flex-direction: column;
            height: calc(100vh - 200px);
            min-height: 500px;
            max-height: 700px;
            overflow: hidden;
            position: relative;
            margin: 0 auto;
            width: 100%;
            max-width: 800px;
        }

        .chat-header {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            padding: 1.25rem;
            font-weight: 600;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
            position: sticky;
            top: 0;
            z-index: 10;
            justify-content: center;
        }

        .chat-header i {
            font-size: 1.2rem;
        }

        .chat-messages {
            flex: 1;
            padding: 1.5rem;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            background-color: #fafcff;
            scroll-behavior: smooth;
        }

        .message {
            max-width: 85%;
            padding: 1rem 1.25rem;
            border-radius: 12px;
            line-height: 1.5;
            position: relative;
            word-wrap: break-word;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            animation: fadeIn 0.3s ease-out;
            margin: 0 auto;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .user-message {
            align-self: flex-end;
            background-color: var(--primary);
            color: white;
            border-bottom-right-radius: 4px;
            margin-right: 0;
        }

        .bot-message {
            align-self: flex-start;
            background-color: white;
            color: var(--dark);
            border: 1px solid var(--light-gray);
            border-bottom-left-radius: 4px;
            margin-left: 0;
        }

        .bot-message strong {
            color: var(--primary);
        }

        .chat-input-container {
            display: flex;
            padding: 1rem;
            background-color: white;
            border-top: 1px solid var(--light-gray);
            position: sticky;
            bottom: 0;
            justify-content: center;
        }

        #message-input {
            flex: 1;
            padding: 0.75rem 1rem;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            outline: none;
            font-size: 1rem;
            transition: var(--transition);
            max-width: 600px;
        }

        #message-input:focus {
            border-color: var(--primary-light);
            box-shadow: 0 0 0 3px rgba(42, 90, 120, 0.1);
        }

        #send-button {
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 8px;
            padding: 0 1.5rem;
            margin-left: 0.75rem;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        #send-button:hover {
            background-color: var(--primary-light);
        }

        /* Typing Indicator */
        .typing-indicator {
            display: flex;
            padding: 1rem;
            align-self: flex-start;
            background-color: white;
            border: 1px solid var(--light-gray);
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            margin: 0 auto;
        }

        .typing-dot {
            width: 10px;
            height: 10px;
            background-color: var(--gray);
            border-radius: 50%;
            margin: 0 3px;
            animation: typingAnimation 1.4s infinite ease-in-out;
        }

        .typing-dot:nth-child(1) {
            animation-delay: 0s;
        }

        .typing-dot:nth-child(2) {
            animation-delay: 0.2s;
        }

        .typing-dot:nth-child(3) {
            animation-delay: 0.4s;
        }

        @keyframes typingAnimation {
            0%, 60%, 100% { transform: translateY(0); }
            30% { transform: translateY(-5px); }
        }

        /* Hidden State */
        .hidden {
            display: none;
        }

        /* Project Card (for demo purposes) */
        .project-card {
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: var(--shadow);
            border-left: 4px solid var(--secondary);
            max-width: 600px;
            margin: 0 auto 1.5rem;
        }

        .project-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            text-align: center;
        }

        .project-card p {
            color: var(--gray);
            margin-bottom: 1rem;
            text-align: center;
        }

        .project-meta {
            display: flex;
            gap: 1rem;
            font-size: 0.9rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .meta-item {
            display: flex;
            align-items: center;
            gap: 0.3rem;
            color: var(--gray);
        }

        /* New Features */
        .feature-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background-color: rgba(212, 167, 98, 0.1);
            color: var(--dark);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
        }

        .feature-badge i {
            color: var(--secondary);
        }

        /* Dark Mode */
        .dark-mode {
            background-color: #121212;
            color: #e0e0e0;
        }

        .dark-mode .home-form,
        .dark-mode .chat-container,
        .dark-mode .project-card {
            background-color: #1e1e1e;
            color: #e0e0e0;
        }

        .dark-mode .bot-message {
            background-color: #2d2d2d;
            color: #e0e0e0;
            border-color: #333;
        }

        .dark-mode .form-control,
        .dark-mode textarea.form-control,
        .dark-mode #message-input {
            background-color: #2d2d2d;
            color: #e0e0e0;
            border-color: #333;
        }

        .dark-mode .option-btn:not(.selected) {
            background-color: #2d2d2d;
            border-color: #333;
            color: #e0e0e0;
        }

        .dark-mode .upload-container {
            border-color: #333;
            background-color: #2d2d2d;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
            z-index: 1000;
            align-items: center;
            justify-content: center;
            animation: fadeIn 0.3s ease-out;
        }

        .modal-content {
            background-color: white;
            border-radius: 12px;
            padding: 2rem;
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            position: relative;
        }

        .dark-mode .modal-content {
            background-color: #1e1e1e;
            color: #e0e0e0;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .modal-title {
            font-size: 1.5rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .dark-mode .modal-title {
            color: var(--secondary);
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--gray);
        }

        /* Login Form */
        .login-form {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .form-row {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .form-row label {
            font-weight: 500;
            color: var(--primary);
        }

        .dark-mode .form-row label {
            color: var(--secondary);
        }

        .form-row input {
            padding: 0.75rem 1rem;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-size: 1rem;
        }

        .dark-mode .form-row input {
            background-color: #2d2d2d;
            color: #e0e0e0;
            border-color: #333;
        }

        .form-actions {
            display: flex;
            justify-content: flex-end;
            gap: 1rem;
            margin-top: 1rem;
        }

        .btn {
            padding: 0.75rem 1.5rem;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            border: none;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-secondary {
            background-color: var(--light-gray);
            color: var(--dark);
        }

        .dark-mode .btn-secondary {
            background-color: #333;
            color: #e0e0e0;
        }

        /* Calculator */
        .calculator {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .calculator-display {
            grid-column: span 4;
            padding: 1rem;
            background-color: var(--light);
            border-radius: 8px;
            text-align: right;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .dark-mode .calculator-display {
            background-color: #2d2d2d;
        }

        .calculator-btn {
            padding: 1rem;
            font-size: 1.2rem;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            background-color: var(--light-gray);
            transition: var(--transition);
        }

        .dark-mode .calculator-btn {
            background-color: #333;
            color: #e0e0e0;
        }

        .calculator-btn.operator {
            background-color: var(--secondary);
            color: white;
        }

        .calculator-btn.equals {
            background-color: var(--primary);
            color: white;
            grid-column: span 2;
        }

        /* Progress Tracker */
        .progress-steps {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .progress-step {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background-color: var(--light);
            border-radius: 8px;
        }

        .dark-mode .progress-step {
            background-color: #2d2d2d;
        }

        .step-checkbox {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        .step-label {
            flex: 1;
        }

        .step-completed {
            text-decoration: line-through;
            color: var(--gray);
        }

        /* Export Options */
        .export-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .export-option {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem;
            background-color: var(--light);
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .dark-mode .export-option {
            background-color: #2d2d2d;
        }

        .export-option:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .export-icon {
            font-size: 2rem;
            color: var(--primary);
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            header {
                padding: 1.5rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .message {
                max-width: 90%;
            }
            
            .option-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }

            .chat-container {
                height: calc(100vh - 150px);
                min-height: 400px;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 10px;
            }
            
            header {
                padding: 1rem;
                border-radius: 8px;
            }
            
            .home-form, .chat-container {
                padding: 1rem;
            }
            
            .form-title {
                font-size: 1.2rem;
            }
            
            .option-btn {
                padding: 0.5rem;
                font-size: 0.8rem;
            }
            
            .feature-badge {
                font-size: 0.75rem;
                padding: 0.4rem 0.8rem;
            }

            .calculator {
                grid-template-columns: repeat(4, 1fr);
            }

            .calculator-btn {
                padding: 0.75rem;
                font-size: 1rem;
            }
        }

        /* Voice Assistant */
        .voice-btn {
            background-color: var(--secondary);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            margin-left: 0.5rem;
            transition: var(--transition);
        }

        .voice-btn:hover {
            transform: scale(1.1);
        }

        .voice-btn.listening {
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(212, 167, 98, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(212, 167, 98, 0); }
            100% { box-shadow: 0 0 0 0 rgba(212, 167, 98, 0); }
        }

        /* Action Buttons */
        .action-btn {
            position: absolute;
            top: 10px;
            border: none;
            border-radius: 6px;
            padding: 0.5rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.3rem;
            font-size: 0.8rem;
            z-index: 5;
            color: white;
        }

        .login-btn {
            right: 10px;
            background-color: var(--gray);
        }

        .dark-mode-toggle {
            right: 120px;
            background-color: var(--dark);
        }

        .export-btn {
            right: 220px;
            background-color: var(--success);
        }

        .progress-tracker {
            right: 320px;
            background-color: var(--primary-light);
        }

        .calculator-btn {
            right: 430px;
            background-color: var(--secondary);
        }

        @media (max-width: 992px) {
            .action-btn {
                position: static;
                margin: 0.5rem;
            }
            
            .chat-header {
                flex-wrap: wrap;
                padding-bottom: 3rem;
            }
        }

        /* Video Tutorials */
        .video-tutorials {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .video-thumbnail {
            background-color: var(--light);
            border-radius: 8px;
            overflow: hidden;
            cursor: pointer;
            transition: var(--transition);
        }

        .dark-mode .video-thumbnail {
            background-color: #2d2d2d;
        }

        .video-thumbnail:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .video-thumbnail-img {
            height: 120px;
            background-color: var(--primary-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
        }

        .video-thumbnail-info {
            padding: 0.75rem;
        }

        .video-thumbnail-title {
            font-weight: 600;
            margin-bottom: 0.25rem;
        }

        .video-thumbnail-duration {
            font-size: 0.8rem;
            color: var(--gray);
        }

        /* Testimonials Section */
        .testimonials {
            margin-top: 2rem;
            padding: 1.5rem;
            background-color: white;
            border-radius: 12px;
            box-shadow: var(--shadow);
            text-align: center;
        }

        .testimonials h3 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .testimonial-card {
            background-color: var(--light);
            padding: 1.5rem;
            border-radius: 8px;
            text-align: left;
            position: relative;
        }

        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 10px;
            left: 10px;
            font-size: 3rem;
            color: rgba(42, 90, 120, 0.1);
            font-family: serif;
            line-height: 1;
        }

        .testimonial-text {
            margin-bottom: 1rem;
            font-style: italic;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .author-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--primary-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .author-info {
            display: flex;
            flex-direction: column;
        }

        .author-name {
            font-weight: 600;
            color: var(--primary);
        }

        .author-title {
            font-size: 0.8rem;
            color: var(--gray);
        }

        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
            padding: 1.5rem;
            background-color: white;
            border-radius: 12px;
            box-shadow: var(--shadow);
            text-align: center;
        }

        .stat-item {
            padding: 1rem;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--gray);
        }

        /* CTA Section */
        .cta-section {
            margin-top: 2rem;
            padding: 2rem;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            border-radius: 12px;
            color: white;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .cta-section h3 {
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .cta-section p {
            margin-bottom: 1.5rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-btn {
            display: inline-block;
            background-color: white;
            color: var(--primary);
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .cta-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.2);
        }

        /* Footer */
        footer {
            margin-top: 3rem;
            padding: 2rem 0;
            text-align: center;
            color: var(--gray);
            font-size: 0.9rem;
            border-top: 1px solid var(--light-gray);
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1rem;
            flex-wrap: wrap;
        }

        .footer-link {
            color: var(--primary);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-link:hover {
            color: var(--primary-light);
            text-decoration: underline;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            transition: var(--transition);
        }

        .social-link:hover {
            background-color: var(--primary);
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="header-content">
                <div class="badge">
                    <i class="fas fa-crown"></i> PREMIUM EDITION
                </div>
                <h1>LUXE Home AI Advisor</h1>
                <p class="tagline">Transform your living space with AI-powered premium home improvement recommendations</p>
                
                <!-- Feature Badges -->
                
            </div>
        </header>

        <div class="app-container">
            <div class="home-form" id="home-form">
                <h2 class="form-title"><i class="fas fa-home"></i> Your Project Details</h2>
                
                <div class="form-group">
                    <label for="rooms">Which rooms would you like to improve?</label>
                    <div class="option-group">
                        <div class="option-grid" id="room-options">
                            <div class="option-btn" data-value="living room">
                                <i class="fas fa-couch"></i>
                                Living Room
                            </div>
                            <div class="option-btn" data-value="kitchen">
                                <i class="fas fa-utensils"></i>
                                Kitchen
                            </div>
                            <div class="option-btn" data-value="bathroom">
                                <i class="fas fa-bath"></i>
                                Bathroom
                            </div>
                            <div class="option-btn" data-value="bedroom">
                                <i class="fas fa-bed"></i>
                                Bedroom
                            </div>
                            <div class="option-btn" data-value="dining room">
                                <i class="fas fa-utensils"></i>
                                Dining
                            </div>
                            <div class="option-btn" data-value="home office">
                                <i class="fas fa-laptop"></i>
                                Office
                            </div>
                            <div class="option-btn" data-value="outdoor">
                                <i class="fas fa-tree"></i>
                                Outdoor
                            </div>
                            <div class="option-btn" data-value="other">
                                <i class="fas fa-plus"></i>
                                Other
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="improvements">Improvement Categories</label>
                    <div class="option-group">
                        <div class="option-grid" id="improvement-options">
                            <div class="option-btn" data-value="cosmetic">
                                <i class="fas fa-paint-roller"></i>
                                Cosmetic
                            </div>
                            <div class="option-btn" data-value="functional">
                                <i class="fas fa-tools"></i>
                                Functional
                            </div>
                            <div class="option-btn" data-value="storage">
                                <i class="fas fa-box-open"></i>
                                Storage
                            </div>
                            <div class="option-btn" data-value="lighting">
                                <i class="fas fa-lightbulb"></i>
                                Lighting
                            </div>
                            <div class="option-btn" data-value="flooring">
                                <i class="fas fa-border-style"></i>
                                Flooring
                            </div>
                            <div class="option-btn" data-value="smart home">
                                <i class="fas fa-robot"></i>
                                Smart Tech
                            </div>
                            <div class="option-btn" data-value="energy">
                                <i class="fas fa-leaf"></i>
                                Energy
                            </div>
                            <div class="option-btn" data-value="luxury">
                                <i class="fas fa-gem"></i>
                                Luxury
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="budget">Project Budget Range</label>
                    <div class="option-group">
                        <div class="budget-options" id="budget-options">
                            <div class="option-btn" data-value="under $500">Under $500</div>
                            <div class="option-btn" data-value="$500-$2,000">$500-$2K</div>
                            <div class="option-btn" data-value="$2,000-$10,000">$2K-$10K</div>
                            <div class="option-btn" data-value="over $10,000">$10K+</div>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="skill-level">Your Skill Level</label>
                    <select id="skill-level" class="form-control">
                        <option value="beginner">Beginner (Simple projects)</option>
                        <option value="intermediate" selected>Intermediate (Some experience)</option>
                        <option value="advanced">Advanced (Complex projects)</option>
                        <option value="professional">Professional Installation</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="style">Preferred Design Style</label>
                    <select id="style" class="form-control">
                        <option value="modern">Modern</option>
                        <option value="contemporary">Contemporary</option>
                        <option value="transitional">Transitional</option>
                        <option value="traditional">Traditional</option>
                        <option value="rustic">Rustic/Farmhouse</option>
                        <option value="industrial">Industrial</option>
                        <option value="scandinavian">Scandinavian</option>
                        <option value="mid-century">Mid-Century Modern</option>
                        <option value="luxury">Luxury</option>
                        <option value="custom">Custom/Other</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="goals">Project Goals & Vision</label>
                    <textarea id="goals" class="form-control" placeholder="Describe what you want to achieve (e.g., 'Modern kitchen with smart appliances', 'Cozy living room with fireplace')"></textarea>
                </div>
                
                <div class="form-group">
                    <label>Upload Room Photos (Optional)</label>
                    <div class="upload-container" id="upload-area">
                        <div class="upload-icon">
                            <i class="fas fa-cloud-upload-alt"></i>
                        </div>
                        <div class="upload-text">
                            Drag & drop photos or click to browse
                        </div>
                        <div class="file-name" id="file-name">No files selected</div>
                        <input type="file" id="image-upload" accept="image/*" multiple>
                    </div>
                </div>
                
                <button class="submit-btn" id="get-recommendations">
                    <i class="fas fa-magic"></i> Generate Premium Recommendations
                </button>

                <!-- Video Tutorials Section -->
                <div style="margin-top: 2rem; border-top: 1px solid var(--light-gray); padding-top: 1.5rem;">
                    <h3 style="color: var(--primary); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem; justify-content: center;">
                        <i class="fas fa-video"></i> Video Tutorials
                    </h3>
                    <div class="video-tutorials">
                        <div class="video-thumbnail" onclick="showVideo('kitchen-remodel')">
                            <div class="video-thumbnail-img">
                                <i class="fas fa-play" style="font-size: 2rem;"></i>
                            </div>
                            <div class="video-thumbnail-info">
                                <div class="video-thumbnail-title">Kitchen Remodel</div>
                                <div class="video-thumbnail-duration">5 min tutorial</div>
                            </div>
                        </div>
                        <div class="video-thumbnail" onclick="showVideo('smart-home')">
                            <div class="video-thumbnail-img">
                                <i class="fas fa-play" style="font-size: 2rem;"></i>
                            </div>
                            <div class="video-thumbnail-info">
                                <div class="video-thumbnail-title">Smart Home Setup</div>
                                <div class="video-thumbnail-duration">8 min tutorial</div>
                            </div>
                        </div>
                        <div class="video-thumbnail" onclick="showVideo('bathroom-renovation')">
                            <div class="video-thumbnail-img">
                                <i class="fas fa-play" style="font-size: 2rem;"></i>
                            </div>
                            <div class="video-thumbnail-info">
                                <div class="video-thumbnail-title">Bathroom Renovation</div>
                                <div class="video-thumbnail-duration">7 min tutorial</div>
                            </div>
                        </div>
                        <div class="video-thumbnail" onclick="showVideo('flooring-installation')">
                            <div class="video-thumbnail-img">
                                <i class="fas fa-play" style="font-size: 2rem;"></i>
                            </div>
                            <div class="video-thumbnail-info">
                                <div class="video-thumbnail-title">Flooring Installation</div>
                                <div class="video-thumbnail-duration">10 min tutorial</div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Testimonials Section -->
                <div class="testimonials">
                    <h3><i class="fas fa-quote-left"></i> What Our Clients Say</h3>
                    <div class="testimonial-grid">
                        <div class="testimonial-card">
                            <div class="testimonial-text">
                                The LUXE Advisor transformed our outdated kitchen into a modern masterpiece. The AI recommendations were spot on and saved us thousands in designer fees.
                            </div>
                            <div class="testimonial-author">
                                <div class="author-avatar">SM</div>
                                <div class="author-info">
                                    <div class="author-name">Sarah M.</div>
                                    <div class="author-title">Homeowner, Chicago</div>
                                </div>
                            </div>
                        </div>
                        <div class="testimonial-card">
                            <div class="testimonial-text">
                                As a contractor, I use LUXE Advisor to provide premium recommendations to my clients. It helps us visualize projects and set realistic budgets.
                            </div>
                            <div class="testimonial-author">
                                <div class="author-avatar">DJ</div>
                                <div class="author-info">
                                    <div class="author-name">David J.</div>
                                    <div class="author-title">Contractor, Miami</div>
                                </div>
                            </div>
                        </div>
                        <div class="testimonial-card">
                            <div class="testimonial-text">
                                The smart home integration suggestions were exactly what we needed. Our house is now both beautiful and technologically advanced.
                            </div>
                            <div class="testimonial-author">
                                <div class="author-avatar">TP</div>
                                <div class="author-info">
                                    <div class="author-name">Tanya P.</div>
                                    <div class="author-title">Tech Enthusiast, Seattle</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Stats Section -->
                <div class="stats">
                    <div class="stat-item">
                        <div class="stat-number">5,000+</div>
                        <div class="stat-label">Happy Clients</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">$25M</div>
                        <div class="stat-label">In Home Improvements</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">92%</div>
                        <div class="stat-label">Satisfaction Rate</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">24/7</div>
                        <div class="stat-label">Support Available</div>
                    </div>
                </div>

                <!-- CTA Section -->
                <div class="cta-section">
                    <h3>Ready to Transform Your Home?</h3>
                    <p>Join thousands of homeowners who have created their dream spaces with LUXE Home AI Advisor.</p>
                    <a href="#" class="cta-btn">Get Started Today</a>
                </div>
            </div>

            <div class="chat-container hidden" id="chat-container">
                <!-- Action Buttons -->
                <button class="action-btn login-btn" id="login-btn">
                    <i class="fas fa-user"></i> Login
                </button>
                <button class="action-btn dark-mode-toggle" id="dark-mode-toggle">
                    <i class="fas fa-moon"></i> Dark
                </button>
                <button class="action-btn export-btn" id="export-btn">
                    <i class="fas fa-file-export"></i> Export
                </button>
                <button class="action-btn progress-tracker" id="progress-tracker">
                    <i class="fas fa-tasks"></i> Progress
                </button>
                <button class="action-btn calculator-btn" id="calculator-btn">
                    <i class="fas fa-calculator"></i> Calculator
                </button>
                
                <div class="chat-header">
                    <i class="fas fa-robot"></i> LUXE Home Advisor
                </div>
                <div class="chat-messages" id="chat-messages">
                    <!-- Demo message for presentation -->
                    <div class="project-card hidden" id="demo-card">
                        <h3>Modern Kitchen Remodel</h3>
                        <p>Transform your kitchen with premium quartz countertops, smart appliances, and custom cabinetry for a luxurious yet functional space.</p>
                        <div class="project-meta">
                            <div class="meta-item">
                                <i class="fas fa-dollar-sign"></i> $15,000-$25,000
                            </div>
                            <div class="meta-item">
                                <i class="fas fa-clock"></i> 4-6 weeks
                            </div>
                            <div class="meta-item">
                                <i class="fas fa-star"></i> 85% ROI
                            </div>
                        </div>
                    </div>
                </div>
                <div class="chat-input-container">
                    <input type="text" id="message-input" placeholder="Ask about premium home improvements...">
                    <button id="send-button">
                        <i class="fas fa-paper-plane"></i>
                    </button>
                    <button class="voice-btn" id="voice-btn">
                        <i class="fas fa-microphone"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer>
            <div class="footer-links">
                <a href="#" class="footer-link">About Us</a>
                <a href="#" class="footer-link">Privacy Policy</a>
                <a href="#" class="footer-link">Terms of Service</a>
                <a href="#" class="footer-link">Contact</a>
                <a href="#" class="footer-link">FAQ</a>
            </div>
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-link"><i class="fab fa-pinterest"></i></a>
                <a href="#" class="social-link"><i class="fab fa-youtube"></i></a>
            </div>
            <p>&copy; 2023 LUXE Home AI Advisor. All rights reserved.</p>
        </footer>
    </div>

    <!-- User Profile Modal -->
    <div class="modal" id="user-profile-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title"><i class="fas fa-user-circle"></i> User Profile</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="login-form">
                <div class="form-row">
                    <label for="login-email">Email</label>
                    <input type="email" id="login-email" placeholder="Enter your email">
                </div>
                <div class="form-row">
                    <label for="login-password">Password</label>
                    <input type="password" id="login-password" placeholder="Enter your password">
                </div>
                <div class="form-actions">
                    <button class="btn btn-secondary close-modal-btn">Cancel</button>
                    <button class="btn btn-primary" id="login-submit">Login</button>
                </div>
                <div style="text-align: center; margin-top: 1rem;">
                    <p>Don't have an account? <a href="#" style="color: var(--primary);">Sign up</a></p>
                </div>
            </div>
        </div>
    </div>

    <!-- Material Calculator Modal -->
    <div class="modal" id="calculator-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title"><i class="fas fa-calculator"></i> Material Calculator</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="calculator-display" id="calc-display">0</div>
            <div class="calculator">
                <button class="calculator-btn" onclick="appendToCalc('7')">7</button>
                <button class="calculator-btn" onclick="appendToCalc('8')">8</button>
                <button class="calculator-btn" onclick="appendToCalc('9')">9</button>
                <button class="calculator-btn operator" onclick="appendToCalc('/')">/</button>
                <button class="calculator-btn" onclick="appendToCalc('4')">4</button>
                <button class="calculator-btn" onclick="appendToCalc('5')">5</button>
                <button class="calculator-btn" onclick="appendToCalc('6')">6</button>
                <button class="calculator-btn operator" onclick="appendToCalc('*')">×</button>
                <button class="calculator-btn" onclick="appendToCalc('1')">1</button>
                <button class="calculator-btn" onclick="appendToCalc('2')">2</button>
                <button class="calculator-btn" onclick="appendToCalc('3')">3</button>
                <button class="calculator-btn operator" onclick="appendToCalc('-')">-</button>
                <button class="calculator-btn" onclick="appendToCalc('0')">0</button>
                <button class="calculator-btn" onclick="appendToCalc('.')">.</button>
                <button class="calculator-btn equals" onclick="calculate()">=</button>
                <button class="calculator-btn operator" onclick="appendToCalc('+')">+</button>
                <button class="calculator-btn" onclick="clearCalc()" style="grid-column: span 4;">Clear</button>
            </div>
            <div style="margin-top: 1.5rem;">
                <h4 style="margin-bottom: 0.5rem;">Material Estimator</h4>
                <select class="form-control" id="material-type">
                    <option value="">Select material type</option>
                    <option value="paint">Paint</option>
                    <option value="flooring">Flooring</option>
                    <option value="tiles">Tiles</option>
                    <option value="drywall">Drywall</option>
                </select>
                <div id="material-inputs" style="margin-top: 1rem;">
                    <!-- Dynamic inputs will appear here -->
                </div>
                <button class="btn btn-primary" style="margin-top: 1rem; width: 100%;" onclick="calculateMaterials()">Calculate</button>
                <div id="material-result" style="margin-top: 1rem; padding: 1rem; background-color: var(--light); border-radius: 8px; display: none;"></div>
            </div>
        </div>
    </div>

    <!-- Progress Tracker Modal -->
    <div class="modal" id="progress-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title"><i class="fas fa-tasks"></i> Project Progress Tracker</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="progress-steps" id="progress-steps">
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step1" checked>
                    <label for="step1" class="step-label step-completed">Initial consultation completed</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step2" checked>
                    <label for="step2" class="step-label step-completed">Design finalized</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step3">
                    <label for="step3" class="step-label">Materials purchased</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step4">
                    <label for="step4" class="step-label">Demolition completed</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step5">
                    <label for="step5" class="step-label">Construction phase 1</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step6">
                    <label for="step6" class="step-label">Construction phase 2</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step7">
                    <label for="step7" class="step-label">Finishing touches</label>
                </div>
                <div class="progress-step">
                    <input type="checkbox" class="step-checkbox" id="step8">
                    <label for="step8" class="step-label">Final inspection</label>
                </div>
            </div>
            <div style="display: flex; justify-content: space-between; margin-top: 1.5rem;">
                <div>
                    <h4>Project Completion</h4>
                    <div style="width: 100%; background-color: var(--light-gray); border-radius: 8px; height: 20px; margin-top: 0.5rem;">
                        <div style="width: 25%; background-color: var(--primary); height: 100%; border-radius: 8px;"></div>
                    </div>
                    <p style="text-align: center; margin-top: 0.5rem;">25% Complete</p>
                </div>
                <button class="btn btn-primary" style="align-self: flex-end;">Save Progress</button>
            </div>
        </div>
    </div>

    <!-- Export Options Modal -->
    <div class="modal" id="export-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title"><i class="fas fa-file-export"></i> Export Options</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="export-options">
                <div class="export-option" onclick="exportProject('pdf')">
                    <div class="export-icon">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <div>PDF Document</div>
                </div>
                <div class="export-option" onclick="exportProject('image')">
                    <div class="export-icon">
                        <i class="fas fa-file-image"></i>
                    </div>
                    <div>Image (PNG)</div>
                </div>
                <div class="export-option" onclick="exportProject('excel')">
                    <div class="export-icon">
                        <i class="fas fa-file-excel"></i>
                    </div>
                    <div>Excel Spreadsheet</div>
                </div>
                <div class="export-option" onclick="exportProject('text')">
                    <div class="export-icon">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <div>Text File</div>
                </div>
                <div class="export-option" onclick="exportProject('print')">
                    <div class="export-icon">
                        <i class="fas fa-print"></i>
                    </div>
                    <div>Print</div>
                </div>
                <div class="export-option" onclick="exportProject('share')">
                    <div class="export-icon">
                        <i class="fas fa-share-alt"></i>
                    </div>
                    <div>Share</div>
                </div>
            </div>
        </div>
    </div>

    <!-- Video Modal -->
    <div class="modal" id="video-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title" id="video-title"><i class="fas fa-video"></i> Video Tutorial</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
                <iframe id="video-iframe" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // DOM elements
            const homeForm = document.getElementById('home-form');
            const chatContainer = document.getElementById('chat-container');
            const chatMessages = document.getElementById('chat-messages');
            const messageInput = document.getElementById('message-input');
            const sendButton = document.getElementById('send-button');
            const getRecsBtn = document.getElementById('get-recommendations');
            const imageUpload = document.getElementById('image-upload');
            const uploadArea = document.getElementById('upload-area');
            const fileName = document.getElementById('file-name');
            const roomOptions = document.querySelectorAll('#room-options .option-btn');
            const improvementOptions = document.querySelectorAll('#improvement-options .option-btn');
            const budgetOptions = document.querySelectorAll('#budget-options .option-btn');
            const demoCard = document.getElementById('demo-card');
            const darkModeToggle = document.getElementById('dark-mode-toggle');
            const voiceBtn = document.getElementById('voice-btn');
            const calculatorBtn = document.getElementById('calculator-btn');
            const progressTracker = document.getElementById('progress-tracker');
            const exportBtn = document.getElementById('export-btn');
            const loginBtn = document.getElementById('login-btn');
            const loginSubmit = document.getElementById('login-submit');
            const videoModal = document.getElementById('video-modal');
            const closeVideoBtn = document.getElementById('close-video');
            const videoIframe = document.getElementById('video-iframe');
            const videoTitle = document.getElementById('video-title');
            
            // Modal elements
            const modals = document.querySelectorAll('.modal');
            const closeModalBtns = document.querySelectorAll('.close-modal, .close-modal-btn');
            
            // API configuration
            const API_KEY = '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';
            const MODEL = 'qwen/qwen2.5-vl-72b-instruct:free';
            
            // Selected options
            let selectedRooms = [];
            let selectedImprovements = [];
            let selectedBudget = '';
            let isListening = false;
            let recognition;
            let conversationHistory = [];
            
            // Initialize option selectors
            function initOptionSelectors() {
                // Room options
                roomOptions.forEach(option => {
                    option.addEventListener('click', function() {
                        this.classList.toggle('selected');
                        const value = this.getAttribute('data-value');
                        
                        if (this.classList.contains('selected')) {
                            if (!selectedRooms.includes(value)) {
                                selectedRooms.push(value);
                            }
                        } else {
                            selectedRooms = selectedRooms.filter(room => room !== value);
                        }
                    });
                });
                
                // Improvement options
                improvementOptions.forEach(option => {
                    option.addEventListener('click', function() {
                        this.classList.toggle('selected');
                        const value = this.getAttribute('data-value');
                        
                        if (this.classList.contains('selected')) {
                            if (!selectedImprovements.includes(value)) {
                                selectedImprovements.push(value);
                            }
                        } else {
                            selectedImprovements = selectedImprovements.filter(imp => imp !== value);
                        }
                    });
                });
                
                // Budget options
                budgetOptions.forEach(option => {
                    option.addEventListener('click', function() {
                        budgetOptions.forEach(opt => opt.classList.remove('selected'));
                        this.classList.add('selected');
                        selectedBudget = this.getAttribute('data-value');
                    });
                });
            }
            
            // File upload handling
            function initFileUpload() {
                // Click on upload area
                uploadArea.addEventListener('click', function() {
                    imageUpload.click();
                });
                
                // Drag and drop
                uploadArea.addEventListener('dragover', function(e) {
                    e.preventDefault();
                    this.style.borderColor = 'var(--primary-light)';
                    this.style.backgroundColor = 'rgba(58, 124, 165, 0.1)';
                });
                
                uploadArea.addEventListener('dragleave', function() {
                    this.style.borderColor = 'var(--light-gray)';
                    this.style.backgroundColor = '';
                });
                
                uploadArea.addEventListener('drop', function(e) {
                    e.preventDefault();
                    this.style.borderColor = 'var(--light-gray)';
                    this.style.backgroundColor = '';
                    
                    if (e.dataTransfer.files.length) {
                        imageUpload.files = e.dataTransfer.files;
                        updateFileName();
                    }
                });
                
                // File input change
                imageUpload.addEventListener('change', updateFileName);
            }
            
            function updateFileName() {
                if (imageUpload.files && imageUpload.files.length > 0) {
                    if (imageUpload.files.length === 1) {
                        fileName.textContent = imageUpload.files[0].name;
                    } else {
                        fileName.textContent = `${imageUpload.files.length} files selected`;
                    }
                    fileName.style.color = 'var(--primary)';
                } else {
                    fileName.textContent = 'No files selected';
                    fileName.style.color = 'var(--gray)';
                }
            }
            
            // Get recommendations button click
            getRecsBtn.addEventListener('click', async function() {
                // Validate selections
                if (selectedRooms.length === 0) {
                    showAlert('Please select at least one room to improve');
                    return;
                }
                
                if (selectedImprovements.length === 0) {
                    showAlert('Please select at least one improvement category');
                    return;
                }
                
                if (!selectedBudget) {
                    showAlert('Please select a budget range');
                    return;
                }
                
                // Get other form values
                const skillLevel = document.getElementById('skill-level').value;
                const style = document.getElementById('style').value;
                const goals = document.getElementById('goals').value;
                const imageFiles = imageUpload.files;
                
                // Show loading state
                getRecsBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Generating...';
                getRecsBtn.disabled = true;
                
                // Create home details message
                let homeDetails = {
                    rooms: selectedRooms,
                    improvements: selectedImprovements,
                    budget: selectedBudget,
                    skillLevel,
                    style,
                    goals
                };
                
                // Add user message to chat
                addMessage('user', formatHomeDetails(homeDetails));
                
                // Hide form and show chat
                homeForm.classList.add('hidden');
                chatContainer.classList.remove('hidden');
                demoCard.classList.add('hidden');
                
                try {
                    // Check if there are images to upload
                    if (imageFiles && imageFiles.length > 0) {
                        const imageUrls = await uploadImages(imageFiles);
                        if (imageUrls && imageUrls.length > 0) {
                            await analyzeImagesAndGenerateRecs(imageUrls, homeDetails);
                        } else {
                            await generateHomeImprovementRecs(homeDetails);
                        }
                    } else {
                        await generateHomeImprovementRecs(homeDetails);
                    }
                } catch (error) {
                    console.error('Error:', error);
                    addMessage('bot', "We apologize for the inconvenience. Our premium service is currently experiencing high demand. Please try again shortly.");
                } finally {
                    getRecsBtn.innerHTML = '<i class="fas fa-magic"></i> Generate Premium Recommendations';
                    getRecsBtn.disabled = false;
                }
            });
            
            // Send message on button click
            sendButton.addEventListener('click', sendMessage);
            
            // Send message on Enter key
            messageInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    sendMessage();
                }
            });
            
            // Function to send a message
            async function sendMessage() {
                const message = messageInput.value.trim();
                if (!message) return;
                
                // Add user message to chat
                addMessage('user', message);
                messageInput.value = '';
                
                // Show typing indicator
                showTypingIndicator();
                
                try {
                    // Add user message to conversation history
                    conversationHistory.push({
                        role: 'user',
                        content: message
                    });
                    
                    // Get AI response
                    const response = await fetchAIResponse(conversationHistory);
                    
                    // Add AI response to conversation history
                    conversationHistory.push({
                        role: 'assistant',
                        content: response
                    });
                    
                    // Add AI message to chat
                    addMessage('bot', response);
                } catch (error) {
                    console.error('Error:', error);
                    addMessage('bot', "We're experiencing high demand on our premium service. Please try your request again.");
                } finally {
                    // Hide typing indicator
                    hideTypingIndicator();
                }
            }
            
            // Function to upload images (mock implementation)
            async function uploadImages(files) {
                return new Promise((resolve) => {
                    const urls = [];
                    const readers = [];
                    
                    for (let i = 0; i < files.length; i++) {
                        readers.push(new FileReader());
                    }
                    
                    let completed = 0;
                    
                    readers.forEach((reader, index) => {
                        reader.onload = (e) => {
                            urls.push(e.target.result);
                            completed++;
                            if (completed === files.length) {
                                resolve(urls);
                            }
                        };
                        reader.readAsDataURL(files[index]);
                    });
                });
            }
            
            // Function to analyze images and generate recommendations
            async function analyzeImagesAndGenerateRecs(imageUrls, homeDetails) {
                showTypingIndicator();
                
                try {
                    // First, analyze the images
                    let imageAnalysisPrompt = `I'm looking for premium home improvement ideas for: ${homeDetails.rooms.join(', ')}. `;
                    imageAnalysisPrompt += `Interested in: ${homeDetails.improvements.join(', ')}. `;
                    imageAnalysisPrompt += `Budget: ${homeDetails.budget}, Style: ${homeDetails.style}, Skill: ${homeDetails.skillLevel}. `;
                    if (homeDetails.goals) imageAnalysisPrompt += `Goals: ${homeDetails.goals}. `;
                    imageAnalysisPrompt += `Analyze these photos and suggest high-end improvements with luxury materials and smart home integration where applicable.`;
                    
                    // Create message with all images
                    const imageMessages = imageUrls.map(url => ({
                        type: 'image_url',
                        image_url: { url }
                    }));
                    
                    const messageContent = [
                        {
                            type: 'text',
                            text: imageAnalysisPrompt
                        },
                        ...imageMessages
                    ];
                    
                    const imageAnalysis = await fetchAIResponse([
                        {
                            role: 'user',
                            content: messageContent
                        }
                    ]);
                    
                    // Add image analysis to chat
                    addMessage('bot', `<strong>LUXE Analysis:</strong>\n\n${imageAnalysis}`);
                    
                    // Then generate additional recommendations
                    await generateHomeImprovementRecs(homeDetails);
                } catch (error) {
                    console.error('Error analyzing images:', error);
                    addMessage('bot', "While we couldn't analyze your images, here are premium recommendations based on your other inputs:");
                    await generateHomeImprovementRecs(homeDetails);
                } finally {
                    hideTypingIndicator();
                }
            }
            
            // Function to generate home improvement recommendations
            async function generateHomeImprovementRecs(homeDetails) {
                showTypingIndicator();
                
                try {
                    // Generate recommendations
                    const recommendations = await fetchAIResponse([
                        {
                            role: 'user',
                            content: formatHomeDetails(homeDetails)
                        }
                    ]);
                    
                    // Add recommendations to chat
                    addMessage('bot', `<strong>Premium Recommendations:</strong>\n\n${recommendations}`);
                } catch (error) {
                    console.error('Error generating recommendations:', error);
                    addMessage('bot', "We're unable to generate recommendations right now. Please try again later.");
                } finally {
                    hideTypingIndicator();
                }
            }
            
            // Function to fetch AI response
            async function fetchAIResponse(messages) {
                const response = await fetch("https://openrouter.ai/api/v1/chat/completions", {
                    method: "POST",
                    headers: {
                        "Authorization": `Bearer ${API_KEY}`,
                        "HTTP-Referer": window.location.href,
                        "X-Title": "LUXE Home AI Advisor",
                        "Content-Type": "application/json"
                    },
                    body: JSON.stringify({
                        "model": MODEL,
                        "messages": messages,
                        "temperature": 0.7
                    })
                });
                
                if (!response.ok) {
                    throw new Error(`API request failed with status ${response.status}`);
                }
                
                const data = await response.json();
                return data.choices[0].message.content;
            }
            
            // Function to add message to chat
            function addMessage(role, content) {
                const messageDiv = document.createElement('div');
                messageDiv.classList.add('message', `${role}-message`);
                
                // Format content with line breaks and strong tags
                let formattedContent = content;
                formattedContent = formattedContent.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>'); // Markdown bold
                formattedContent = formattedContent.replace(/\n/g, '<br>'); // Line breaks
                
                messageDiv.innerHTML = formattedContent;
                chatMessages.appendChild(messageDiv);
                chatMessages.scrollTop = chatMessages.scrollHeight;
            }
            
            // Function to show typing indicator
            function showTypingIndicator() {
                const typingDiv = document.createElement('div');
                typingDiv.classList.add('typing-indicator');
                typingDiv.id = 'typing-indicator';
                typingDiv.innerHTML = `
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                `;
                chatMessages.appendChild(typingDiv);
                chatMessages.scrollTop = chatMessages.scrollHeight;
            }
            
            // Function to hide typing indicator
            function hideTypingIndicator() {
                const typingIndicator = document.getElementById('typing-indicator');
                if (typingIndicator) {
                    typingIndicator.remove();
                }
            }
            
            // Function to format home details
            function formatHomeDetails(details) {
                let message = `Provide premium home improvement recommendations with these details:
- <strong>Rooms:</strong> ${details.rooms.join(', ')}
- <strong>Improvements:</strong> ${details.improvements.join(', ')}
- <strong>Budget:</strong> ${details.budget}
- <strong>Skill Level:</strong> ${details.skillLevel}
- <strong>Style:</strong> ${details.style}`;
                
                if (details.goals) {
                    message += `\n- <strong>Goals:</strong> ${details.goals}`;
                }
                
                message += `\n\nFocus on luxury materials, high-end finishes, and premium solutions. Include smart home integration where applicable. Provide cost estimates, timeline, and potential ROI for each recommendation.`;
                
                return message;
            }
            
            // Function to show alert
            function showAlert(message) {
                const alertDiv = document.createElement('div');
                alertDiv.style.position = 'fixed';
                alertDiv.style.top = '20px';
                alertDiv.style.left = '50%';
                alertDiv.style.transform = 'translateX(-50%)';
                alertDiv.style.backgroundColor = 'var(--primary)';
                alertDiv.style.color = 'white';
                alertDiv.style.padding = '12px 24px';
                alertDiv.style.borderRadius = '8px';
                alertDiv.style.boxShadow = '0 4px 12px rgba(0,0,0,0.15)';
                alertDiv.style.zIndex = '1000';
                alertDiv.style.animation = 'fadeIn 0.3s ease-out';
                alertDiv.textContent = message;
                
                document.body.appendChild(alertDiv);
                
                setTimeout(() => {
                    alertDiv.style.animation = 'fadeOut 0.3s ease-out';
                    setTimeout(() => {
                        document.body.removeChild(alertDiv);
                    }, 300);
                }, 3000);
            }
            
            // Initialize the app
            initOptionSelectors();
            initFileUpload();
            
            // Add demo card for presentation
            setTimeout(() => {
                demoCard.classList.remove('hidden');
            }, 500);

            // Modal functionality
            function openModal(modalId) {
                document.getElementById(modalId).style.display = 'flex';
                document.body.style.overflow = 'hidden';
            }

            function closeModal(modalId) {
                document.getElementById(modalId).style.display = 'none';
                document.body.style.overflow = 'auto';
            }

            // Close modals when clicking outside
            modals.forEach(modal => {
                modal.addEventListener('click', function(e) {
                    if (e.target === modal) {
                        closeModal(modal.id);
                    }
                });
            });

            // Close modals when clicking close buttons
            closeModalBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    const modal = this.closest('.modal');
                    closeModal(modal.id);
                });
            });

            // Dark mode toggle
            darkModeToggle.addEventListener('click', function() {
                document.body.classList.toggle('dark-mode');
                if (document.body.classList.contains('dark-mode')) {
                    darkModeToggle.innerHTML = '<i class="fas fa-sun"></i> Light';
                    localStorage.setItem('darkMode', 'enabled');
                } else {
                    darkModeToggle.innerHTML = '<i class="fas fa-moon"></i> Dark';
                    localStorage.setItem('darkMode', 'disabled');
                }
            });

            // Check for saved dark mode preference
            if (localStorage.getItem('darkMode') === 'enabled') {
                document.body.classList.add('dark-mode');
                darkModeToggle.innerHTML = '<i class="fas fa-sun"></i> Light';
            }

            // Voice recognition
            voiceBtn.addEventListener('click', toggleVoiceRecognition);

            function toggleVoiceRecognition() {
                if (!isListening) {
                    startVoiceRecognition();
                } else {
                    stopVoiceRecognition();
                }
            }

            function startVoiceRecognition() {
                if ('webkitSpeechRecognition' in window) {
                    recognition = new webkitSpeechRecognition();
                    recognition.continuous = false;
                    recognition.interimResults = false;

                    recognition.onstart = function() {
                        isListening = true;
                        voiceBtn.classList.add('listening');
                        messageInput.placeholder = "Listening...";
                    };

                    recognition.onresult = function(event) {
                        const transcript = event.results[0][0].transcript;
                        messageInput.value = transcript;
                        voiceBtn.classList.remove('listening');
                        isListening = false;
                        messageInput.placeholder = "Ask about premium home improvements...";
                    };

                    recognition.onerror = function(event) {
                        console.error('Voice recognition error', event.error);
                        voiceBtn.classList.remove('listening');
                        isListening = false;
                        messageInput.placeholder = "Ask about premium home improvements...";
                        showAlert("Voice recognition error. Please try again.");
                    };

                    recognition.onend = function() {
                        if (isListening) {
                            recognition.start();
                        } else {
                            voiceBtn.classList.remove('listening');
                            messageInput.placeholder = "Ask about premium home improvements...";
                        }
                    };

                    recognition.start();
                } else {
                    showAlert("Voice recognition not supported in your browser");
                }
            }

            function stopVoiceRecognition() {
                if (recognition) {
                    recognition.stop();
                }
                isListening = false;
                voiceBtn.classList.remove('listening');
                messageInput.placeholder = "Ask about premium home improvements...";
            }

            // Calculator functionality
            calculatorBtn.addEventListener('click', function() {
                openModal('calculator-modal');
            });

            let calcValue = '0';

            function appendToCalc(value) {
                if (calcValue === '0' && value !== '.') {
                    calcValue = value;
                } else {
                    calcValue += value;
                }
                document.getElementById('calc-display').textContent = calcValue;
            }

            function clearCalc() {
                calcValue = '0';
                document.getElementById('calc-display').textContent = calcValue;
            }

            function calculate() {
                try {
                    const result = eval(calcValue);
                    calcValue = result.toString();
                    document.getElementById('calc-display').textContent = calcValue;
                } catch (error) {
                    showAlert("Invalid calculation");
                    clearCalc();
                }
            }

            // Material calculator
            document.getElementById('material-type').addEventListener('change', function() {
                const materialInputs = document.getElementById('material-inputs');
                materialInputs.innerHTML = '';
                
                switch(this.value) {
                    case 'paint':
                        materialInputs.innerHTML = `
                            <div class="form-row">
                                <label for="paint-area">Wall Area (sq ft)</label>
                                <input type="number" id="paint-area" placeholder="Enter wall area">
                            </div>
                            <div class="form-row">
                                <label for="paint-coats">Number of Coats</label>
                                <input type="number" id="paint-coats" value="2" min="1">
                            </div>
                            <div class="form-row">
                                <label for="paint-coverage">Paint Coverage (sq ft/gallon)</label>
                                <input type="number" id="paint-coverage" value="350" min="1">
                            </div>
                        `;
                        break;
                    case 'flooring':
                        materialInputs.innerHTML = `
                            <div class="form-row">
                                <label for="floor-area">Floor Area (sq ft)</label>
                                <input type="number" id="floor-area" placeholder="Enter floor area">
                            </div>
                            <div class="form-row">
                                <label for="floor-waste">Waste Percentage (%)</label>
                                <input type="number" id="floor-waste" value="10" min="0" max="100">
                            </div>
                        `;
                        break;
                    case 'tiles':
                        materialInputs.innerHTML = `
                            <div class="form-row">
                                <label for="tile-area">Area to Tile (sq ft)</label>
                                <input type="number" id="tile-area" placeholder="Enter area">
                            </div>
                            <div class="form-row">
                                <label for="tile-size">Tile Size (inches)</label>
                                <input type="text" id="tile-size" placeholder="e.g. 12x12" value="12x12">
                            </div>
                            <div class="form-row">
                                <label for="tile-waste">Waste Percentage (%)</label>
                                <input type="number" id="tile-waste" value="10" min="0" max="100">
                            </div>
                        `;
                        break;
                    case 'drywall':
                        materialInputs.innerHTML = `
                            <div class="form-row">
                                <label for="drywall-area">Wall Area (sq ft)</label>
                                <input type="number" id="drywall-area" placeholder="Enter wall area">
                            </div>
                            <div class="form-row">
                                <label for="drywall-sheets">Sheet Size</label>
                                <select id="drywall-sheets">
                                    <option value="32">4x8 ft (32 sq ft)</option>
                                    <option value="48">4x12 ft (48 sq ft)</option>
                                </select>
                            </div>
                            <div class="form-row">
                                <label for="drywall-waste">Waste Percentage (%)</label>
                                <input type="number" id="drywall-waste" value="10" min="0" max="100">
                            </div>
                        `;
                        break;
                }
            });

            function calculateMaterials() {
                const materialType = document.getElementById('material-type').value;
                const resultDiv = document.getElementById('material-result');
                resultDiv.style.display = 'block';
                
                switch(materialType) {
                    case 'paint':
                        const area = parseFloat(document.getElementById('paint-area').value) || 0;
                        const coats = parseFloat(document.getElementById('paint-coats').value) || 2;
                        const coverage = parseFloat(document.getElementById('paint-coverage').value) || 350;
                        const gallons = Math.ceil((area * coats) / coverage);
                        resultDiv.innerHTML = `
                            <strong>Paint Needed:</strong> ${gallons} gallon(s)<br>
                            <small>Coverage: ${coverage} sq ft/gallon, ${coats} coat(s)</small>
                        `;
                        break;
                    case 'flooring':
                        const floorArea = parseFloat(document.getElementById('floor-area').value) || 0;
                        const waste = parseFloat(document.getElementById('floor-waste').value) || 10;
                        const totalFlooring = Math.ceil(floorArea * (1 + waste/100));
                        resultDiv.innerHTML = `
                            <strong>Flooring Needed:</strong> ${totalFlooring} sq ft<br>
                            <small>Including ${waste}% waste factor</small>
                        `;
                        break;
                    case 'tiles':
                        const tileArea = parseFloat(document.getElementById('tile-area').value) || 0;
                        const tileSize = document.getElementById('tile-size').value;
                        const tileWaste = parseFloat(document.getElementById('tile-waste').value) || 10;
                        const [width, height] = tileSize.split('x').map(Number);
                        const tileSqFt = (width * height) / 144; // Convert to sq ft
                        const tilesNeeded = Math.ceil((tileArea * (1 + tileWaste/100)) / tileSqFt);
                        resultDiv.innerHTML = `
                            <strong>Tiles Needed:</strong> ${tilesNeeded} tiles<br>
                            <small>Tile size: ${tileSize} inches, ${tileWaste}% waste factor</small>
                        `;
                        break;
                    case 'drywall':
                        const drywallArea = parseFloat(document.getElementById('drywall-area').value) || 0;
                        const sheetSize = parseFloat(document.getElementById('drywall-sheets').value) || 32;
                        const drywallWaste = parseFloat(document.getElementById('drywall-waste').value) || 10;
                        const sheetsNeeded = Math.ceil((drywallArea * (1 + drywallWaste/100)) / sheetSize);
                        resultDiv.innerHTML = `
                            <strong>Drywall Sheets Needed:</strong> ${sheetsNeeded} sheets<br>
                            <small>Sheet size: ${sheetSize === 32 ? '4x8 ft' : '4x12 ft'}, ${drywallWaste}% waste factor</small>
                        `;
                        break;
                    default:
                        resultDiv.innerHTML = 'Please select a material type';
                }
            }

            // Progress tracker
            progressTracker.addEventListener('click', function() {
                openModal('progress-modal');
            });

            // Update progress when checkboxes are clicked
            document.querySelectorAll('.step-checkbox').forEach(checkbox => {
                checkbox.addEventListener('change', function() {
                    const label = this.nextElementSibling;
                    if (this.checked) {
                        label.classList.add('step-completed');
                    } else {
                        label.classList.remove('step-completed');
                    }
                    updateProgressBar();
                });
            });

            function updateProgressBar() {
                const checkboxes = document.querySelectorAll('.step-checkbox');
                const completed = Array.from(checkboxes).filter(cb => cb.checked).length;
                const total = checkboxes.length;
                const percentage = Math.round((completed / total) * 100);
                
                document.querySelector('#progress-modal .progress-step + div div div').style.width = `${percentage}%`;
                document.querySelector('#progress-modal .progress-step + div p').textContent = `${percentage}% Complete`;
            }

            // Export options
            exportBtn.addEventListener('click', function() {
                openModal('export-modal');
            });

            function exportProject(type) {
                let message = '';
                switch(type) {
                    case 'pdf':
                        message = 'Generating PDF document...';
                        break;
                    case 'image':
                        message = 'Exporting as PNG image...';
                        break;
                    case 'excel':
                        message = 'Creating Excel spreadsheet...';
                        break;
                    case 'text':
                        message = 'Exporting as text file...';
                        break;
                    case 'print':
                        message = 'Preparing for printing...';
                        window.print();
                        break;
                    case 'share':
                        message = 'Opening share options...';
                        if (navigator.share) {
                            navigator.share({
                                title: 'LUXE Home Improvement Plan',
                                text: 'Check out my home improvement plan created with LUXE Advisor',
                                url: window.location.href
                            }).catch(err => {
                                console.error('Error sharing:', err);
                            });
                        } else {
                            showAlert("Web Share API not supported in your browser");
                        }
                        break;
                }
                
                if (type !== 'share') {
                    showAlert(message);
                }
                closeModal('export-modal');
            }

            // User profile/login
            loginBtn.addEventListener('click', function() {
                openModal('user-profile-modal');
            });

            loginSubmit.addEventListener('click', function() {
                const email = document.getElementById('login-email').value;
                const password = document.getElementById('login-password').value;
                
                if (!email || !password) {
                    showAlert('Please enter both email and password');
                    return;
                }
                
                // Mock login - in a real app you would validate credentials with a server
                showAlert(`Welcome back, ${email.split('@')[0]}!`);
                loginBtn.innerHTML = `<i class="fas fa-user"></i> ${email.split('@')[0]}`;
                closeModal('user-profile-modal');
            });

            // Video tutorials
            function showVideo(videoId) {
                let videoUrl = '';
                let title = '';
                
                switch(videoId) {
                    case 'kitchen-remodel':
                        videoUrl = 'https://www.youtube.com/embed/example1';
                        title = 'Kitchen Remodel Tutorial';
                        break;
                    case 'smart-home':
                        videoUrl = 'https://www.youtube.com/embed/example2';
                        title = 'Smart Home Setup Guide';
                        break;
                    case 'bathroom-renovation':
                        videoUrl = 'https://www.youtube.com/embed/example3';
                        title = 'Bathroom Renovation Guide';
                        break;
                    case 'flooring-installation':
                        videoUrl = 'https://www.youtube.com/embed/example4';
                        title = 'Flooring Installation Tutorial';
                        break;
                }
                
                videoIframe.src = videoUrl;
                videoTitle.textContent = title;
                openModal('video-modal');
            }

            // Check for PWA install prompt
            let deferredPrompt;
            window.addEventListener('beforeinstallprompt', (e) => {
                e.preventDefault();
                deferredPrompt = e;
                
                // Show install prompt
                setTimeout(() => {
                    const prompt = document.createElement('div');
                    prompt.className = 'install-prompt';
                    prompt.innerHTML = `
                        <div>
                            <i class="fas fa-download" style="color: var(--primary);"></i>
                            Install LUXE Advisor for better experience
                        </div>
                        <button id="install-btn">Install</button>
                    `;
                    document.body.appendChild(prompt);
                    
                    document.getElementById('install-btn').addEventListener('click', () => {
                        prompt.style.animation = 'slideUp 0.5s ease-out reverse';
                        setTimeout(() => {
                            prompt.remove();
                        }, 500);
                        
                        deferredPrompt.prompt();
                        deferredPrompt.userChoice.then((choiceResult) => {
                            if (choiceResult.outcome === 'accepted') {
                                console.log('User accepted install prompt');
                            } else {
                                console.log('User dismissed install prompt');
                            }
                            deferredPrompt = null;
                        });
                    });
                }, 5000);
            });
        });
    </script>
</body>
</html>
