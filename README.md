# DockerElixir19Release - Multi-stage Docker Builds and Elixir 1.9 Releases

From:

https://akoutmos.com/post/multipart-docker-and-elixir-1.9-releases/

    $ mix deps.get

    $ docker run --name my_app --publish 4000:4000 --env COOL_TEXT='ELIXIR ROCKS!!!!' --env SECRET_KEY_BASE=$(mix phx.gen.secret) --env APP_PORT=4000 docker_elixir1:latest

    $ docker exec -it my_app bash

    $ ./prod/rel/docker_elixir_19_release/bin/docker_elixir_19_release remote

Agora que temos um shell IEx remoto conectado ao nosso aplicativo em execução, você pode iniciar o observador da CLI executando o seguinte.

    > :observer_cli.start()

![Imagem do Observer cli](https://akoutmos.com/img/docker_elixir_19/observer_cli.png)



  * Install dependencies with `mix deps.get`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Learn more

  * Official website: https://www.phoenixframework.org/
  * Guides: https://hexdocs.pm/phoenix/overview.html
  * Docs: https://hexdocs.pm/phoenix
  * Forum: https://elixirforum.com/c/phoenix-forum
  * Source: https://github.com/phoenixframework/phoenix
