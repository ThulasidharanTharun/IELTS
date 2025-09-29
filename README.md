# IELTS
IELTS Home page 


import React, { useState } from 'react';

const IELTSInstitute = () => {
  const [isMenuOpen, setIsMenuOpen] = useState(false);

  // Feature cards data
  const features = [
    {
      title: "Speaking Practice",
      description: "One-on-one sessions with certified IELTS examiners to boost your speaking confidence",
      icon: (
        <svg xmlns="http://www.w3.org/2000/svg" className="h-12 w-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z" />
        </svg>
      )
    },
    {
      title: "Mock Tests",
      description: "Full-length practice exams that mirror the real IELTS test format and difficulty",
      icon: (
        <svg xmlns="http://www.w3.org/2000/svg" className="h-12 w-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
        </svg>
      )
    },
    {
      title: "AI Band Score",
      description: "Instant feedback on your writing and speaking with our advanced AI scoring system",
      icon: (
        <svg xmlns="http://www.w3.org/2000/svg" className="h-12 w-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
        </svg>
      )
    },
    {
      title: "Expert Guidance",
      description: "Personalized study plans from IELTS experts with proven track records",
      icon: (
        <svg xmlns="http://www.w3.org/2000/svg" className="h-12 w-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
        </svg>
      )
    }
  ];

  // Testimonials data
  const testimonials = [
    {
      name: "Sarah Johnson",
      score: "Band 8.5",
      text: "The personalized speaking sessions helped me overcome my anxiety. I went from Band 6 to Band 8.5 in just 3 months!",
      avatar: "SJ"
    },
    {
      name: "Michael Chen",
      score: "Band 7.0",
      text: "The AI writing feedback was incredibly detailed. It pointed out mistakes I never would have noticed on my own.",
      avatar: "MC"
    },
    {
      name: "Emma Rodriguez",
      score: "Band 8.0",
      text: "The mock tests were spot-on with the real exam. I felt completely prepared on test day thanks to their realistic practice materials.",
      avatar: "ER"
    }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-blue-50 to-white">
      {/* Navbar */}
      <nav className="bg-white shadow-sm">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex justify-between h-16">
            <div className="flex items-center">
              <div className="flex-shrink-0 flex items-center">
                <div className="bg-blue-600 text-white font-bold text-xl p-2 rounded-md">IELTS</div>
                <span className="ml-2 text-xl font-bold text-gray-900">Academy Pro</span>
              </div>
              <div className="hidden md:ml-10 md:flex md:space-x-8">
                <a href="#" className="text-blue-600 border-b-2 border-blue-600 px-1 pt-1 text-sm font-medium">Home</a>
                <a href="#" className="text-gray-500 hover:text-gray-700 px-1 pt-1 text-sm font-medium">Courses</a>
                <a href="#" className="text-gray-500 hover:text-gray-700 px-1 pt-1 text-sm font-medium">Testimonials</a>
                <a href="#" className="text-gray-500 hover:text-gray-700 px-1 pt-1 text-sm font-medium">Resources</a>
                <a href="#" className="text-gray-500 hover:text-gray-700 px-1 pt-1 text-sm font-medium">Contact</a>
              </div>
            </div>
            <div className="flex items-center">
              <div className="hidden md:ml-4 md:flex md:items-center">
                <button className="ml-4 px-4 py-2 border border-transparent text-sm font-medium rounded-md text-blue-700 bg-blue-100 hover:bg-blue-200">
                  Sign In
                </button>
                <button className="ml-4 px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
                  Get Started
                </button>
              </div>
              <div className="-mr-2 flex items-center md:hidden">
                <button
                  onClick={() => setIsMenuOpen(!isMenuOpen)}
                  className="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none"
                >
                  <svg className="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d={isMenuOpen ? "M6 18L18 6M6 6l12 12" : "M4 6h16M4 12h16M4 18h16"} />
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>

        {/* Mobile menu */}
        {isMenuOpen && (
          <div className="md:hidden">
            <div className="pt-2 pb-3 space-y-1">
              <a href="#" className="bg-blue-50 border-blue-500 text-blue-700 block pl-3 pr-4 py-2 border-l-4 text-base font-medium">Home</a>
              <a href="#" className="border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700 block pl-3 pr-4 py-2 border-l-4 text-base font-medium">Courses</a>
              <a href="#" className="border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700 block pl-3 pr-4 py-2 border-l-4 text-base font-medium">Testimonials</a>
              <a href="#" className="border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700 block pl-3 pr-4 py-2 border-l-4 text-base font-medium">Resources</a>
              <a href="#" className="border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700 block pl-3 pr-4 py-2 border-l-4 text-base font-medium">Contact</a>
            </div>
            <div className="pt-4 pb-3 border-t border-gray-200">
              <div className="flex items-center px-4">
                <button className="w-full px-4 py-2 border border-transparent text-sm font-medium rounded-md text-blue-700 bg-blue-100 hover:bg-blue-200">
                  Sign In
                </button>
                <button className="ml-3 w-full px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
                  Get Started
                </button>
              </div>
            </div>
          </div>
        )}
      </nav>

      {/* Hero Section */}
      <div className="relative bg-white overflow-hidden">
        <div className="max-w-7xl mx-auto">
          <div className="relative z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-2xl lg:w-full lg:pb-28 xl:pb-32">
            <main className="mt-10 mx-auto max-w-7xl px-4 sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
              <div className="sm:text-center lg:text-left">
                <h1 className="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
                  <span className="block">Master IELTS with</span>
                  <span className="block text-blue-600">Expert Guidance</span>
                </h1>
                <p className="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">
                  Join thousands of students who achieved their dream scores with our proven IELTS preparation system. Personalized learning paths, expert instructors, and AI-powered feedback.
                </p>
                <div className="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
                  <div className="rounded-md shadow">
                    <a
                      href="#"
                      className="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 md:py-4 md:text-lg md:px-10"
                    >
                      Start Free Trial
                    </a>
                  </div>
                  <div className="mt-3 sm:mt-0 sm:ml-3">
                    <a
                      href="#"
                      className="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-blue-700 bg-blue-100 hover:bg-blue-200 md:py-4 md:text-lg md:px-10"
                    >
                      View Courses
                    </a>
                  </div>
                </div>
              </div>
            </main>
          </div>
        </div>
        <div className="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
          <div className="h-56 w-full bg-blue-500 sm:h-72 md:h-96 lg:w-full lg:h-full flex items-center justify-center">
            <div className="bg-gray-200 border-2 border-dashed rounded-xl w-full h-full max-w-2xl flex items-center justify-center">
              <span className="text-gray-500 text-lg">IELTS Preparation Illustration</span>
            </div>
          </div>
        </div>
      </div>

      {/* Features Section */}
      <div className="py-12 bg-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center">
            <h2 className="text-base font-semibold text-blue-600 tracking-wide uppercase">Our Approach</h2>
            <p className="mt-2 text-3xl font-extrabold text-gray-900 sm:text-4xl">
              Comprehensive IELTS Preparation
            </p>
            <p className="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto">
              Everything you need to achieve your target band score
            </p>
          </div>

          <div className="mt-10">
            <div className="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
              {features.map((feature, index) => (
                <div key={index} className="pt-6">
                  <div className="flow-root bg-gray-50 rounded-lg px-6 pb-8">
                    <div className="-mt-6">
                      <div>
                        <span className="inline-flex items-center justify-center p-3 bg-blue-500 rounded-md shadow-lg">
                          {feature.icon}
                        </span>
                      </div>
                      <h3 className="mt-8 text-lg font-medium text-gray-900 tracking-tight">{feature.title}</h3>
                      <p className="mt-5 text-base text-gray-500">
                        {feature.description}
                      </p>
                    </div>
                  </div>
                </div>
              ))}
            </div>
          </div>
        </div>
      </div>

      {/* Testimonials Section */}
      <div className="bg-blue-50 py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center">
            <h2 className="text-base font-semibold text-blue-600 tracking-wide uppercase">Student Success</h2>
            <p className="mt-2 text-3xl font-extrabold text-gray-900 sm:text-4xl">
              What Our Students Say
            </p>
          </div>

          <div className="mt-10">
            <div className="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
              {testimonials.map((testimonial, index) => (
                <div key={index} className="bg-white rounded-lg shadow-lg p-6">
                  <div className="flex items-center">
                    <div className="flex-shrink-0">
                      <div className="bg-blue-100 rounded-full w-12 h-12 flex items-center justify-center">
                        <span className="text-blue-800 font-bold">{testimonial.avatar}</span>
                      </div>
                    </div>
                    <div className="ml-4">
                      <h4 className="text-lg font-bold text-gray-900">{testimonial.name}</h4>
                      <p className="text-blue-600 font-medium">{testimonial.score}</p>
                    </div>
                  </div>
                  <div className="mt-4">
                    <p className="text-gray-600 italic">"{testimonial.text}"</p>
                  </div>
                  <div className="mt-6 flex">
                    {[...Array(5)].map((_, i) => (
                      <svg key={i} className="w-5 h-5 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    ))}
                  </div>
                </div>
              ))}
            </div>
          </div>
        </div>
      </div>

      {/* CTA Section */}
      <div className="bg-blue-600">
        <div className="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:py-16 lg:px-8 lg:flex lg:items-center lg:justify-between">
          <h2 className="text-3xl font-extrabold tracking-tight text-white sm:text-4xl">
            <span className="block">Ready to boost your IELTS score?</span>
            <span className="block text-blue-200">Start your journey today.</span>
          </h2>
          <div className="mt-8 flex lg:mt-0 lg:flex-shrink-0">
            <div className="inline-flex rounded-md shadow">
              <a
                href="#"
                className="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-blue-600 bg-white hover:bg-blue-50"
              >
                Get started
              </a>
            </div>
            <div className="ml-3 inline-flex rounded-md shadow">
              <a
                href="#"
                className="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-700 hover:bg-blue-800"
              >
                Learn more
              </a>
            </div>
          </div>
        </div>
      </div>

      {/* Footer */}
      <footer className="bg-gray-800">
        <div className="max-w-7xl mx-auto py-12 px-4 overflow-hidden sm:px-6 lg:px-8">
          <nav className="-mx-5 -my-2 flex flex-wrap justify-center" aria-label="Footer">
            {['Home', 'Courses', 'Testimonials', 'Resources', 'Contact'].map((item) => (
              <div key={item} className="px-5 py-2">
                <a href="#" className="text-base text-gray-300 hover:text-white">
                  {item}
                </a>
              </div>
            ))}
          </nav>
          <div className="mt-8 flex justify-center space-x-6">
            {[0, 1, 2, 3].map((item) => (
              <a key={item} href="#" className="text-gray-400 hover:text-gray-300">
                <span className="sr-only">Social media</span>
                <div className="h-6 w-6 bg-gray-400 rounded-full"></div>
              </a>
            ))}
          </div>
          <div className="mt-8 text-center">
            <p className="text-base text-gray-400">
              &copy; 2023 IELTS Academy Pro. All rights reserved.
            </p>
            <p className="mt-2 text-sm text-gray-500">
              123 Education Street, Learning City, LC 10001
            </p>
            <p className="mt-1 text-sm text-gray-500">
              contact@ieltsacademypro.com | (123) 456-7890
            </p>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default IELTSInstitute;
