<script setup>
import Project from '@/components/Project.vue'

const projects = [
  {
    title: 'Custom LED Controller',
    description: 'I made an LED controller based on the ESP32 along with a companion Android app. The app supports a varity of patterns to customize. My favorites where soft color transitions and the rolling red, white, and blue just like on the news.',
    date: 'Summer 2020',
    imageUrl: 'https://via.placeholder.com/300x200',
    skills: ['C++', 'FreeRTOS', 'Android Development', 'Bluetooth', 'Circuit Design', 'Soldering'],
    links: [
      'https://github.com/Lazloian/LEDControllerV2']
  },
  {
    title: 'Robot Driver HUD and Ammo Detector',
    description: 'I created a simple heads up display using a transparent LED screen for the Purdue Robomaster team. The screen showed warnings for low ammo and blind spot detection. I made a custom controller board and ammo detector that integrated into the robot\'s ammo hopper.',
    date: 'Fall 2019',
    imageUrl: 'https://via.placeholder.com/300x200',
    skills: ['PCB Design', 'Embedded C'],
    links: [
      'https://github.com/PurdueRM/Electrical-System/tree/master/Heads-Up-Display-ToF']
  },
  {
    title: 'Static Site Generator',
    description: 'When making my first website as a teenager, I had the genius and original idea of translating markdown files into html so I could easily add content to the website (I never head of a static site generator before). The tool can upload content to the server, list/remove posts, and update the site.',
    date: 'Summer 2020',
    imageUrl: 'https://via.placeholder.com/300x200',
    skills: ['Linux', 'Shell Scripting', 'HTML'],
    links: [
        'https://github.com/Lazloian/henrysilva.xyz']
  },
  {
    title: 'Dog Sleep Tracker',
    description: 'I wanted to know how much my dog slept in a day. I used an ESP32 with an accelerometer to track movement and a raspberry pi running Node-RED and Grafana to visualize the data. A custom circuit board and 3D printed case made it possible to attach to my dog\'s collar.',
    date: 'Summer 2019',
    imageUrl: 'https://via.placeholder.com/300x200',
    skills: ['ESP32', 'C++', 'Raspberry Pi', 'Node-RED', 'CAD', '3D Printing'],
    links: [
        'https://github.com/Lazloian/DogWifi']
  },
  {
    title: 'Robotics Curriculum',
    description: 'I made a 10-week robotics curriculum for junior high students to introduce them to the basics of robotics and programming using the Lego Mindstorms platform. The curriculum included slides for each lesson including small activities to teach concepts. 4 group competitions had teams apply lesson concepts to a game.',
    date: 'Summer 2019',
    imageUrl: 'https://via.placeholder.com/300x200',
    skills: ['Effective Communication', 'Teaching', 'Game Design', 'Powerpoint'],
    links: [
        'https://github.com/Lazloian/DogWifi']
  },
]
</script>

<template>
<section class="max-w-6xl mx-auto py-8 space-y-12">
    <h2 class="text-3xl font-semibold text-white mb-6">Personal Projects</h2>
    <Project v-for="project in projects" :key="project.title" :project="project" />
</section>
</template>