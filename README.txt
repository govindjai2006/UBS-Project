#####################################################################
UBS pre-interview task for position: Senior Software Engineer .NET C#
#####################################################################

Maint Task:
	Use existing project template and implement next requirements:
	
	UBS_TransformService:
	-	Implement WCF Service for UBS_TransformService.Services.ICurrencyTransform
		as contract (TCP binging);
	-	Use Topshelf library to run CurrencyTransform service;


	UBS_API:
	-	Create WCF TCP communication between UBS_API and UBS_TransformService;
	-	Create controller to expose Humanize() method as POST API call. 
		Allowed return codes: 200, 400, 500.
		Implement possible edge case cheks.
	-	Add Entity framework Code first data layer to store corversions done
		and use them as cache in API created before calling WCF conversion 
		(use SQLite DB Provider). Use LINQ Method call style to querry DB;
	-	Add Swagger (Swashbuckle) as UI to be available in Debug build only;

	Target framework: .Net Framevork v.4.6.1
	Both projects are assumet to be running on same host
	Use git to commit implementation step-by-step.

#####################################################################

Additional Tasks (optional):
	-	Add Unit testing (MSTest v2);
	-	Add documentation comments;
	-	Add authorization for API controller for any local user;
	-	Extract data layer into separate solution;
	-	Implement conversion of Humanize() method yourself;
	-	Add angular[.js] UI to use API created and host it as static from UBS_API runtime:
		        Extrapoints
        - Gulp Build (concat and minify both css and js files)
        - Keep code modular using ControllerAs syntax
        - AJAX Requests using promises via a factory service
        - Toasters to handle API response message(s)
        - Type safe and sanity checking on request and response
        - Use component architecture where needed for future angular versions
        - Good use of design and css [Absolutely NO UBS Branding or references]

#####################################################################

Pack implementation into .zip archive and send for review.

#####################################################################