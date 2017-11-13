package be.steformations.pc.ticketmaster.jobs;

import be.steformations.pc.ticketmaster.ejb.EjbTicketMasterService;

@javax.ejb.Singleton
@javax.ejb.Startup
public class TicketMasterCleaningJob {

	@javax.ejb.EJB
	private EjbTicketMasterService ejbService;
	
	@javax.ejb.Schedule(hour="8",minute="30",second="0")
	public void execute(javax.ejb.Timer timer) {
		this.ejbService.cleanShows();
		timer.cancel();
	}
}
