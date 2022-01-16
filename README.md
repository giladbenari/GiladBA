# GiladBA
Currency Convertor
## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Prerequisites](#Prerequisites)
* [Running_the_application](#Running_the_application)
* [How_To_Use_(SPA)](#How_To_Use_(SPA))
* [Features (Implementation)](#Features (Implementation))

## General info
This project is and On-Line Currency Convertor.
	
## Technologies
Project is created with:
* This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.0.4.
* Installed Material library 

	
## Prerequisites
To use this project, install it locally using npm:
* make sure you the correct angular version  (13.0.4)
* also have Material library (ng add @angular/material)


## Running_the_application
* Download the app (src.rar) and extract it
* Make sure all libraries exists (npm materials)
* run command ng start (or ng s)

## How_To_Use_(SPA)
* First page hold the currencies convertor: 1. choose two currencies, 2. choose amount 3. click on "Convert": calculation appears
* Second page is the Converting History: all converting history appears. To DELETE history, click on "Clear History"


## Features (Implementation)
Folder CurrencyList
* Holds two components
* First is the Currency Convertor - where the user can convert currencies
* Second is the History. Please note that the HISTORY WILL NOT BE DELETED ON REFRESH (Bonus)
* To delete the History please click on "Clear History" button
Services
* CurrencyExchangeWebApiService - all the WEB API calls (get, post, promise). the calls are GENERIC
  so the observables and the interceptor handle the incoming data and errors
* JwtInterceptor - service handle all web api calls: headers, TOKEN validations and errors (e.g. HTTP error and other errors) 
* AuthGuard - handle the validation of users to access routing (client side)
* GeneralErrorHandlerService - general error handling (been called automaticlly from Interceptor on error)
* LocalStorageService - handle the client cache (add, delete, get...).
Models
* This part part hold data models and DTO (e.g. messages, URLs and so on)
* DTO - all strings: storageKey, URL, date Format ....
* IExchangesRatesModel - data model
