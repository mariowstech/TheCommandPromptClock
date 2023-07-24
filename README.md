# TheCommandPromptClock
An useless clock made in batch, but its cool.
This shit is the updated version of my old one.

## How does this bitch works?
We need to split this in three parts, startup, clock, reset.

### 1) Startup sequence
```
@echo off   <-- Removes the prompt part;
title The Command Prompt Clock - Made by mariowstech!   <-- Set the window title;
@mode con colss=30 lines=7   <-- Set the window resolution;
color 02   <-- Set the text color, which is green.
```
### 2) The actual clock
```
:main   <-- Where we are;
cls     <-- Clear window;
echo The Command Prompt Clock                               <-- Title;
echo =====================================================
echo Time: %time%                                           <-- Shows the time with the echo command;
echo Date: %date%                                           <-- Shows the date with the echo command;
echo =====================================================
echo made with hate by mariowstech!                         <-- yes.
```
### 3) Refresh part
```
ping -n 2 0.0.0.0>nul     <-- This is the core part, which pings an unvalid IP adress, and refreshes the window, so that all of the commands will be re-displayed;
goto main                 <-- This is where the commands are, so when refreshed, goes into that location.
```
Not the hardest to understand.

## Made with hate by mariowstech!
