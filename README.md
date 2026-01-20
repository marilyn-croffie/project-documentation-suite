# MavPASS Scheduling Project Documentation

Complete technical documentation suite for the MavPASS (Maverick Peer-Facilitated Academic Support System) automated scheduling project at Minnesota State University, Mankato.

## Project Overview

MavPASS operates over 100 peer-facilitated study sessions weekly across multiple courses. The manual scheduling process—coordinating leader availability, room capacity, course schedules, and optimal session timing—was time-intensive and error-prone. This project developed a genetic algorithm-based solution to automate schedule generation while satisfying complex constraints.

## Documentation Suite

This repository contains the complete project documentation developed by the MavPASS Scheduling Team:

### Core Technical Documents

- **Requirements Analysis Document** - System requirements, current state analysis, and functional specifications
- **Database Design Document** - Relational database schema, entity relationships, and normalization strategy
- **Fitness Scores Document** - Detailed scoring metrics for soft constraints (ISN 2a-5) and genetic algorithm fitness function
- **Test Plan Document** - Testing strategy, defect tracking procedures, and quality assurance framework

### Project Management Documents

- **Handover Document** - Comprehensive project overview, timeline, deliverables, scope changes, and transition planning
- **User Documentation** - Installation guide, system requirements, and operational procedures for end users

## Key Technical Contributions

**Genetic Algorithm Implementation**
- Custom fitness function balancing 5 weighted constraints (leader variety, course distribution, optimal timing, time windows, room capacity)
- Hard constraints prevent invalid schedules; soft constraints optimize quality
- Achieved 88% fitness score vs. 76% for manual schedules

**Database Architecture**
- Normalized relational schema (MySQL) modeling courses, leaders, rooms, sessions, and availability
- Bit-string representation for efficient availability matching
- Entity relationships supporting complex scheduling logic

**Constraint Modeling**
- ISN 2a: Leader schedule variety (10% weight)
- ISN 3: Course session distribution (20% weight)
- ISN 4a: Optimal timing relative to lectures (35% weight - highest priority)
- ISN 4b: Preferred time windows (15% weight)
- ISN 5: Room capacity matching (20% weight)

**Testing Framework**
- Unit testing for core functions
- Defect severity classification and tracking protocols
- Alpha/beta testing strategy

## Technical Stack

- **Language:** C#
- **Database:** MySQL
- **IDE:** Visual Studio 2022
- **Testing:** nUnit
- **Version Control:** GitHub
- **Export Format:** Excel (Day/Room/Master schedules)

## Team

**MavPASS Scheduling Team (Fall 2022)**
- Marilyn Croffie - Team Lead
- Madeline Ellingson - Software Engineer
- Justin Engels - Database Engineer
- Hiruy Gebregiorgis - Test Engineer

**Faculty Coach:** Dr. Lin Chase  
**Subject Matter Expert:** Dr. John Burke  
**Clients:** Dr. Laura Jacobi (MavPASS Faculty Liaison), Lina Wang (MavPASS Coordinator)

## Project Outcomes

- Reduced scheduling time from days to ~5 minutes
- Improved schedule quality from 76% to 88% fitness
- Eliminated manual spreadsheet manipulation
- Generated optimized schedules in three Excel formats
- Documented complete system for Phase 2 development

## Future Work

Phase 2 recommendations include:
- Web-based UI development
- MavConnect integration for automated room availability
- Modularized constraint system for easier updates
- Performance optimization (sub-minute generation)
- Comprehensive automated testing suite

## Repository Structure

```
├── Requirements Analysis Document.pdf
├── Database Design Document.pdf
├── Fitness Scores Document.pdf
├── Test Plan Document.pdf
├── Handover Document.pdf
└── User Documentation.pdf
```

## Context

This documentation represents a project demonstrating software engineering principles including requirements analysis, database design, algorithm development, testing methodology, and professional technical writing. The project successfully delivered a working proof-of-concept that improved upon the existing manual process.
