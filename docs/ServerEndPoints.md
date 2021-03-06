## Fetching Skills

Request type: GET

To fetch a list of skills you can use this end point.Output comes as one object.

    http://api.susi.ai/cms/getSkillList.json

You can pass filter your output by passing like this:

    http://api.susi.ai/cms/getSkillList.json?model=MODEL_VALUE&group=GROUP_VALUE&language=LANGUAGE_VALUE

sample query:

    http://api.susi.ai/cms/getSkillList.json?model=general&group=Knowledge&language=xx

From this endpoint you can get you can get a sorted list of all skills. This producess a array of skills

    http://api.susi.ai/cms/getSkillList.json?applyFilter=true&filter_name=ascending&filter_type=lexicographical

If you need you can mix up sorting parameters with filtering parameters like this.

    http://api.susi.ai/cms/getSkillList.json?model=MODEL_VALUE&group=GROUP_VALUE&applyFilter=true&filter_name=ascending&filter_type=lexicographical

## Fetching Skills by Authors

Request type: GET

If you need to get a list of skills made by one specific user, you can use this endpoint.

    http://api.susi.ai/cms/getSkillsByAuthor.json?author=AUTHOR_NAME

## Fetching Skills groups

Request type: GET

If you need to get all the skill groups you can use this endpoint.

    http://api.susi.ai/cms/getGroups.json

## Fetching all languages

Request type: GET

If you need to get all the skill languages you can use this endpoint.

    http://api.susi.ai/cms/getAllLanguages.json

## Create a Skill

Request type: POST

Data: 
    ```
    {
        model: MODEL_VALUE,
        group: GROUP_VALUE,
        language: LANGUAGE,
        skill: SKILL_NAME,
        image: IMAGE_FILE,
        content:SKILL_CODE,
        image_name: IMAGE_NAME,
        access_token: ACCESS_TOKEN
    }
    ```

    http://api.susi.ai/cms/createSkill.json