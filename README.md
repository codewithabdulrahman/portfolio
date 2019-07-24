https://angularfirebase.com/lessons/sharing-data-between-angular-components-four-methods/


<strong> Data Service</strong>

import { Injectable } from '@angular/core';
import { BehaviorSubject } from 'rxjs';

@Injectable()
export class DataService {

  private messageSource = new BehaviorSubject('defaul message');
  currentMessage = this.messageSource.asObservable();

  constructor() { }

  changeMessage(message: string) {
    this.messageSource.next(message)
  }
}

<strong> App Component.ts</strong>

import { Component } from '@angular/core';
import {DataService} from "./services/DataServices";

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'my-app';
  message1="";
  message:string;

  constructor(private data: DataService) { }

  ngOnInit() {
    this.data.currentMessage.subscribe(message => this.message = message)
  }
  receiveMessage($event){
    this.message1=$event;
    console.log(this.message);
  }
}

<strong> Child Component.ts</strong>

import { Component, OnInit,Output,EventEmitter } from '@angular/core';
import {DataService} from "../services/DataServices";

@Component({
  selector: 'app-child-component',
  templateUrl: './child-component.component.html',
  styleUrls: ['./child-component.component.css']
})
export class ChildComponentComponent implements OnInit {
  message: string = "Hallow";
  constructor(private data:DataService) { }

  ngOnInit() {

  }

  @Output() messageEvent=new EventEmitter<string>();
  sendMessage(){
    this.messageEvent.emit(this.message);
  }
  sendServiceData(){
    this.data.changeMessage("Mza O Mza");
  }
}

