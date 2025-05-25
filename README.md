    header {
        background-color: #2c3e50;
        color: white;
        text-align: center;
        padding: 1rem;
        box-shadow: 0 2px 8px rgba(0,0,0,0.3); /* Stronger shadow */
        position: relative; /* For wave effect if added later */
        animation: slideInTop 1s forwards cubic-bezier(0.23, 1, 0.32, 1); /* Slide in from top */
    }

    .profile-section {
        text-align: center;
        margin-top: 30px; /* More space from header */
        animation: fadeInScale 1s forwards cubic-bezier(0.175, 0.885, 0.32, 1.275) 0.5s; /* Fade in and slight bounce */
        opacity: 0; /* Start hidden for animation */
    }

    .profile-section img {
        width: 140px; /* Slightly larger image */
        height: 140px;
        border-radius: 50%;
        object-fit: cover;
        border: 5px solid #fff; /* Thicker white border */
        box-shadow: 0 0 20px rgba(0,0,0,0.2); /* Enhanced shadow */
        transition: transform 0.3s ease-in-out; /* Smooth hover effect */
    }

    .profile-section img:hover {
        transform: scale(1.05) rotate(2deg); /* Subtle rotate on hover */
    }

    .profile-section h1 {
        font-size: 2.8rem; /* Larger name */
        margin-top: 15px;
        color: #2c3e50;
        text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        animation: slideInRight 1s forwards ease-out 0.8s; /* Slide in name */
        opacity: 0;
    }

    .profile-section p {
        font-size: 1.2rem; /* Larger description */
        color: #555;
        margin-bottom: 25px;
        animation: slideInLeft 1s forwards ease-out 1s; /* Slide in description */
        opacity: 0;
    }

    .container {
        flex-grow: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 25px;
        padding: 20px;
    }

    h2 {
        font-size: 2.5rem; /* Larger call to action */
        margin-bottom: 30px;
        color: #2c3e50;
        text-align: center;
        animation: fadeInSlideUp 1s forwards cubic-bezier(0.25, 0.46, 0.45, 0.94) 1.5s; /* Fade in and slide up */
        opacity: 0;
    }

    .social-links {
        display: flex;
        flex-direction: column;
        gap: 20px; /* More space between buttons */
        width: 90%;
        max-width: 450px; /* Slightly wider max width */
        animation: staggerFadeInUp 1.5s forwards ease-out 1.8s; /* Staggered animation for links */
        opacity: 0; /* Start hidden for animation */
    }

    .social-links a {
        display: flex;
        align-items: center;
        padding: 18px 30px; /* Larger padding for buttons */
        background-color: #3498db;
        color: white;
        text-decoration: none;
        border-radius: 10px; /* More rounded corners */
        font-size: 1.3rem; /* Larger font size */
        font-weight: bold;
        transition: background-color 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease, filter 0.3s ease; /* Added filter transition */
        box-shadow: 0 6px 12px rgba(0,0,0,0.2); /* Stronger shadow */
        transform-origin: center; /* For bounce effect */
        animation: bounceIn 0.8s backwards cubic-bezier(0.175, 0.885, 0.32, 1.275); /* Individual bounce in */
    }

    .social-links a:hover {
        background-color: #2980b9;
        transform: translateY(-5px) scale(1.02); /* More pronounced lift and slight scale */
        box-shadow: 0 8px 16px rgba(0,0,0,0.25);
        filter: brightness(1.1); /* Slightly brighten on hover */
    }

    .social-links a i {
        margin-right: 18px; /* More space for icon */
        font-size: 1.6rem; /* Larger icon size */
        animation: rotateIn 0.8s backwards ease-out; /* Icon rotation on load */
    }

    /* Specific colors for social media buttons */
    .social-links a.youtube { background-color: #FF0000; }
    .social-links a.youtube:hover { background-color: #cc0000; }
    .social-links a.tiktok { background-color: #000000; }
    .social-links a.tiktok:hover { background-color: #222222; }
    .social-links a.instagram {
        background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); /* Instagram gradient */
    }
    .social-links a.instagram:hover {
        filter: brightness(1.2); /* Brighten the gradient */
        transform: translateY(-5px) scale(1.02);
    }

    footer {
        background-color: #2c3e50;
        color: white;
        text-align: center;
        padding: 1rem;
        width: 100%;
        margin-top: auto;
        box-shadow: 0 -2px 8px rgba(0,0,0,0.3);
        animation: slideInBottom 1s forwards cubic-bezier(0.23, 1, 0.32, 1) 2.5s; /* Slide in from bottom */
        opacity: 0;
    }

    /* Keyframes for animations */

    @keyframes slideInTop {
        0% { transform: translateY(-100%); opacity: 0; }
        100% { transform: translateY(0); opacity: 1; }
    }

    @keyframes slideInBottom {
        0% { transform: translateY(100%); opacity: 0; }
        100% { transform: translateY(0); opacity: 1; }
    }

    @keyframes fadeInScale {
        0% { opacity: 0; transform: scale(0.8); }
        100% { opacity: 1; transform: scale(1); }
    }

    @keyframes slideInRight {
        0% { opacity: 0; transform: translateX(50px); }
        100% { opacity: 1; transform: translateX(0); }
    }

    @keyframes slideInLeft {
        0% { opacity: 0; transform: translateX(-50px); }
        100% { opacity: 1; transform: translateX(0); }
    }

    @keyframes fadeInSlideUp {
        0% { opacity: 0; transform: translateY(30px); }
        100% { opacity: 1; transform: translateY(0); }
    }

    /* Staggered animation for social links */
    /* This animation is applied to the .social-links container,
       and then individual link delays are handled with animation-delay in JS
       or by applying a custom property (like below) and calculating.
       For this pure CSS example, we'll apply a base animation and individual delays.
    */
    .social-links a:nth-child(1) { animation-delay: 1.8s; } /* YouTube */
    .social-links a:nth-child(2) { animation-delay: 2.0s; } /* TikTok */
    .social-links a:nth-child(3) { animation-delay: 2.2s; } /* Instagram */
    /* Add more if you add more links */

    @keyframes bounceIn {
        0%, 20%, 40%, 60%, 80%, 100% {
            transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
        }
        0% { opacity: 0; transform: scale3d(.3, .3, .3); }
        20% { transform: scale3d(1.1, 1.1, 1.1); }
        40% { transform: scale3d(.9, .9, .9); }
        60% { opacity: 1; transform: scale3d(1.03, 1.03, 1.03); }
        80% { transform: scale3d(.97, .97, .97); }
        100% { opacity: 1; transform: scale3d(1, 1, 1); }
    }

    @keyframes rotateIn {
        0% {
            transform-origin: center;
            transform: rotate3d(0, 0, 1, -200deg);
            opacity: 0;
        }
        100% {
            transform-origin: center;
            transform: none;
            opacity: 1;
        }
    }


    /* Responsive adjustments */
    @media (max-width: 600px) {
        .profile-section img {
            width: 100px;
            height: 100px;
        }
        .profile-section h1 {
            font-size: 2.2rem;
        }
        .profile-section p {
            font-size: 1rem;
        }
        h2 {
            font-size: 1.9rem;
        }
        .social-links a {
            font-size: 1.1rem;
            padding: 15px 20px;
        }
        .social-links a i {
            font-size: 1.4rem;
            margin-right: 12px;
        }
    }
</style>
