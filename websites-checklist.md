# Websites

### 1. Browserstack tests
- [ ] Desktop: test on latest versions of Chrome, IE/Edge, Firefox, Safari
- [ ] Mobile: test on latest versions of Mobile Safari, Android

### 2. Frontend checklist

#### Assets
- [ ] Search sources for `http://`. Replace by `https://`
- [ ] Lint (s)css sources
- [ ] Webfonts: is the live domain configured in services like Typekit, Fonts.com etc.?
- [ ] Is the browserlist properly configured for autoprefixer and babel-preset-env?
- [ ] When using PurgeCSS: check if layout is preserved.
- [ ] Use optimized assets https://tinyjpg.com/

#### Scripts
- [ ] Is `yarn.lock` present?
- [ ] Check JS lint errors. Remove all `console.log` lines in scripts
- [ ] Check for console errors

#### Page weight
- [ ] Evaluate total weight of at least homepage
- [ ] Open Inspector network/timeline tab to identify heavy assets 
- [ ] Check if heavy assets are cached 

#### Performance
- [ ] Use the Chrome DevTools and throttle your CPU and network with 10x CPU slowdown and set the network to "Good 3G".
- [ ] Google Page Speed score of 90+ https://testmysite.withgoogle.com

#### Security
- [ ] Follow best practices
- [ ] Check cross-site scripting
- [ ] Check cross-site request forgery

#### Check content (with an open console)
- [ ] Are all strings / images present (and translated)?
- [ ] Does menu/submenu have a correct active state on every page?
- [ ] Are 404, 500 and 503 pages provided? Do they provide useful content like 'back to home', search or a navigation tree?
- [ ] Check all pages for n+1 problems

#### Meta
- [ ] Check page titles / descriptions
- [ ] Test Facebook sharing. Provide og-tags if needed
- [ ] Does Favicon load? Pin the tab in Safari to check pinned icon

#### Components
- [ ] Google Maps
    - [ ] API key needed/configured?
    - [ ] Check info windows
    - [ ] Prevent zoom out beyond 1x world
    - [ ] Try clicking on markers
- [ ] Forms: fill out with wrong/right values
- [ ] Video: check with sound on
- [ ] Remove/Uninstall unused component/modules
- [ ] Dev dependencies are not part of production build?
- [ ] Analytics needed/configured?
- [ ] Error monitoring https://www.bugsnag.com/ needed/configured?

#### Server, DNS & Services
- [ ] Add redirects from old to new pages if necessary.
- [ ] Install Let's Encrypt certificate
- [ ] Check SSL certificate health https://www.ssllabs.com/ssltest/
- [ ] Try visiting `www` domain, should redirect to `non-www`
- [ ] Try out visiting `http`, should redirect to `https`
- [ ] Verify that the content of robots header is current with `curl-I https://url` on `x-robots-tag`
- [ ] Remove development DNS record
- [ ] Check dns propagation with https://www.whatsmydns.net/
- [ ] Verify Tag Manager / Analytics have been correctly set up

#### Google Search Console
- [ ] Submit all www/non-www http/https variations
- [ ] Set up non-www https as the preferred domain 
- [ ] Crawl > Fetch as Google > Submit to index to kickstart index

### 3. Services & Tools
- [ ] List of all services & tools.
- [ ] If using a Client's services get access to them (Test & Live API keys)
- [ ] Is the url being monitored by our uptime-monitor?
- [ ] Is the server being monitored by our server-monitor?