peregrineCMS Business Template
---


to deploy this business sample website into a running peregrine instance (needs peregrine-cms:issues/93 and themeclean-flex:feature/contentrestructure branches): 

```
# deploy the business sample

git clone https://github.com/peregrine-cms/business-sample
cd business-sample
npm run deploy

```

to start a sling instance for this business sample: 

```
git clone https://github.com/headwirecom/peregrine-cms
git clone https://github.com/headwirecom/themeclean-flex

cd peregrine-cms
git checkout issues/93
cd ..

cd themeclean-flex
git checkout feature/contentrestructure
cd ..

cd peregrine-cms
cd resources

# start peregrine

windows:
start java -jar com.peregrine-cms.sling.launchpad-9.1.jar
cd ..
cd ..

mac:
java -jar com.peregrine-cms.sling.launchpad-9.1.jar &
cd ..
cd ..

# build peregrine

cd peregrine-cms
percli compile -d
cd ..

# build themecleanflex

cd themeclean-flex
percli compile -d
cd ..
```
