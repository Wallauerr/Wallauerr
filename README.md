```elixir
defmodule Developer.Wallauerr do
  @moduledoc "Vinícius Wallauer · Full Stack Developer · Backend focus"

  def profile do
    %{}
    |> about_me()
    |> socials()
    |> currently()
    |> skills()
  end

  defp about_me(profile) do
    Map.merge(profile, %{
      name: "Vinícius Wallauer",
      role: "Full Stack Developer",
      focus: :backend,
      locality: "Rio Grande do Sul, Brazil",
      english: :intermediate,
      work: true,
      open_to_work: true,
      email: "wallauer@protonmail.com"
    })
  end

  defp socials(profile) do
    Map.merge(profile, %{
      linkedin: "linkedin.com/in/vinicius-wallauer"
    })
  end

  defp currently(profile) do
    Map.merge(profile, %{
      building: ["SaaS", "Web Platforms", "Developer Tools"],
      exploring: ["System Design", "Fluent English"]
    })
  end

  defp skills(profile) do
    Map.merge(profile, %{
      languages: ~w(Elixir TypeScript JavaScript Python SQL),
      backend: ~w(Phoenix LiveView Ecto Fastify Node.js REST JWT Zod),
      frontend: ~w(React Next.js TailwindCSS shadcn/ui TanStack Vite Electron GSAP),
      databases: ["PostgreSQL", "Drizzle ORM", "SQLite"],
      testing: ~w(ExUnit ExMachina Mox Bypass Vitest Supertest),
      infrastructure: ["Docker", "GitHub Actions", "Linux"]
    })
  end
end
```
