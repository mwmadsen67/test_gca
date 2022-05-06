# add aliases
alias bi="bundle install"
alias ber="bundle exec rspec"
# git change authorship - run command with name and email to get credit for all commits
function gca() {
    git filter-branch -f --env-filter "GIT_AUTHOR_NAME='$1'; GIT_AUTHOR_EMAIL='$2'; GIT_COMMITTER_NAME='$1'; GIT_COMMITTER_EMAIL='$2';" HEAD
}
export FILTER_BRANCH_SQUELCH_WARNING=1