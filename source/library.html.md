---
layout: library

title: Library Class Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - ruby

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>

search: true
---

# Engine

## request_ride(RideRequest)

## commit(TransitState)

## attach_module(EngineModule)

# EngineModule (Config)

## handle_request

# OnDemandModule

## initialize(OnDemandConfig)

# BookAheadModule

## initialize(BookAheadConfig)

# DispatchZone

# DirectionsProvider

## retrieve_directions

# OsrmLocalDirectionsProvider

# VrpSolver

## calculate(vrp_model)

# OrToolsLocalVrpSolver

# VrpModel

## add_visit(order_id, location, demand, arrival, departure)

## add_pickup_and_delivery(visit_id)

# RoadManager

# Metastructure

# TransitNetwork

## routes

## stops

## trips

## corridors

## edges

## calendar

## source_corridors

```ruby
network.source_corridors
```

## target_corridors

```ruby
network.target_corridors
```

## trips_in_edge(edge_id)

```ruby
network.trips_in_edge(id)
```

## depots

```ruby
network.depots
```

# Pathfinder

## time_remaining_to_point(point)

## planned_position_after_time_traveled(interval)

## on_path?

## on_time?

# Simulator

## time_travel

## pause

## process_event

## scenes

## add_agent_ai(ai)

# OsrmLocalDirectionsProvider

# VrpSolver

# DriverAgentAI

## initialize(driver, engine)

## act

# EventSource

## consume_until(time)

# StreamingEventSource

# DemandSampler

## assign_outcome

## make_region

## sample

# RideRequest

## origin

## destination

## preferred_arrival
  
# Booking

## pickup_time_range

## dropoff_time_range

## boarding_stop

## alighting_stop

## status (booked waiting riding fulfilled)

## journey_duration

## planned_journey_duration

## wait_duration

## planned_wait_duration

# ResourceScheduler

## set_available(resource_id, start_time, end_time)

## available_at?(resource_id, start_time, end_time=nil)

# Rerouter

## initialize(trip, directions_provider)

# TransitNetworkAnalysis

# Reports::DispatchSession

# Reports::RiderQualityOfService

# GTFSTransitNetwork

## load_gtfs!

## write_gtfs

# Pathfinder

## time_remaining_to_point(point)

## planned_position_after_time_traveled(interval)

## on_path?

## on_time?

# TripPlan

## bookings_for_visit(visit_id)

## next_visit

## max_passenger_volume