To run your local instance of documentation to test or develop, use following commands:

```
git clone "https://review.rdoproject.org/r/rdo-infra/rdo-mkdocs-website"
cd /rdo-mkdocs-website
virtualenv website
. website/bin/activate
pip install mkdocs-material
mkdocs serve
```
