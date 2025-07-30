## implementation in Cargo.toml
```Rust
[dependencies]
thiserror = "1.0"
```

#### This module helps to reduce boilerplate while <span style="color:#ffffff">implementing Error messages</span> 

```Rust
use std::error;
use thiserror::Error;

#[derive(Error, Debug)]
enum TicketNewError {

	#[error("Title cannot be empty")]
	TitleCannotBeEmpty,
	  
	#[error("Title cannot be longer than 50 bytes")]
	TitleTooLong,
	
	#[error("Description cannot be empty")]
	DescriptionCannotBeEmpty,
	
	#[error("Description cannot be longer than 500 bytes")]
	DescriptionTooLong,
}
#[derive(Debug, PartialEq, Clone)]

struct Ticket {
title: String,
description: String,
status: Status,
}
#[derive(Debug, PartialEq, Clone)]
enum Status {
	ToDo,
	InProgress { assigned_to: String },
	Done,
} 
impl Ticket {
	pub fn new(
		title: String,
		description: String,
		status: Status,
		) -> Result<Ticket, TicketNewError> {
		if title.is_empty() {
			return Err(TicketNewError::TitleCannotBeEmpty);
		}
		if title.len() > 50 {
			return Err(TicketNewError::TitleTooLong);
		}
		if description.is_empty() {
			return Err(TicketNewError::DescriptionCannotBeEmpty);
		}
		if description.len() > 500 {
			return Err(TicketNewError::DescriptionTooLong);
		}
		  
		Ok(Ticket {
			title,
			description,
			status,
		})
	}
}
```