# Versioning

Rather than hardcoding a version number in the request URL, you can control which version of the API
you want to access directly from your [application dashboard](https://developer.fabriq.io).  You can
override this value in individual requests by setting the HTTP header X-FABRIQ-API-VERSION.

For example:

<code style="display:block;text-align:center;margin-top:20px;color:#000;padding:10px;">
X-FABRIQ-API-VERSION: v1
</code>

<br>

The current version is **v1** and new versions will be created when backward-incompatible changes
are introduced to the API.  Refer to the [developer portal](https://developer.fabriq.io)
for details of changes between API versions.


<br>

<aside class="warning">
The API is currently in <b><i>beta</i></b>.  In this release, only sandbox client_id's will be generated in
the developer portal.  Live-mode client_id's will be made available once the API is fully released.
</aside>
