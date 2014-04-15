# A Micro-Framework in Shine

```

import Presenter from "swarm.app"

module Hello include Presenter
   @self.route('GET', '/:whom')
   greet(req, args, query)
      hdrs = { }
      hdrs['Content-Type'] = 'text/plain'
      mesg = "Hello %{args.whom or 'World'}!"
      return { 200, hdrs, { mesg } }
   end
end

Hello.run()

```

