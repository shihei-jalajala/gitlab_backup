# Backup GitLab

## GitLabのバックアップ対象

- (1)GitLab構成情報
- (2)GitLabアプリケーションデータ


## Dockerコンテナのバックアップ方法

https://docs.gitlab.com/ee/raketasks/backup_restore.html#creating-a-backup-of-the-gitlab-system

If you are running GitLab within a Docker container, you can run the backup from the host:

```
docker exec -t <container name> gitlab-backup create
```

## 構成ファイルのパス

- [Install GitLab using docker-compose](https://docs.gitlab.com/omnibus/docker/#install-gitlab-using-docker-compose)
- [Storing configuration files](https://docs.gitlab.com/ee/raketasks/backup_restore.html#storing-configuration-files)

> For Docker installations, you must back up the volume where the configuration files are stored. If you have created the GitLab container according to the documentation, it should be under /srv/gitlab/config.

docker-compose.ymlで構成ファイル `/srv/gitlab/config` ディレクトリをボリュームマウントしてるのでパスを確認する

## refs

- [GitLabのバックアップを取ってみた #gitlab #gitlabjp](https://www.creationline.com/lab/22705)
- [Install GitLab using docker-compose](https://docs.gitlab.com/omnibus/docker/#install-gitlab-using-docker-compose)
- [Storing configuration files](https://docs.gitlab.com/ee/raketasks/backup_restore.html#storing-configuration-files)

