```mathematica
1.9M └─┬ main
932K   ├─┬ wordium
904K   │ ├─┬ Deps
440K   │ │ ├── g_api.txt
244K   │ │ ├── rood_lhf.txt
108K   │ │ ├── dns_sub_permutate.txt
104K   │ │ ├── fuzz_mini.txt
4.0K   │ │ └── README.md
 20K   │ ├── wordium.sh
4.0K   │ └── README.md
664K   ├─┬ misc
224K   │ ├─┬ Github
216K   │ │ ├─┬ Runners
 84K   │ │ │ ├─┬ Ubuntu
 20K   │ │ │ │ ├── 0xf_gh_runner_ubuntu_debug.yaml
 16K   │ │ │ │ ├── 0xf_gh_runner_ubuntu_ng_no_ts_debug.yaml
8.0K   │ │ │ │ ├── setup_tailscale.sh
8.0K   │ │ │ │ ├── ngrok_tg_ssh.sh
8.0K   │ │ │ │ ├── debloat.sh
8.0K   │ │ │ │ ├── 0xf_gh_runner_ubuntu_vanilla.yaml
8.0K   │ │ │ │ ├── 0xf_gh_runner_ubuntu_toolpacker.yaml
4.0K   │ │ │ │ └── ipv6_warp.sh
 84K   │ │ │ ├─┬ Self-Hosted
 16K   │ │ │ │ ├── x86_64-ubuntu.dockerfile
 16K   │ │ │ │ ├── ubuntu-systemd-base.dockerfile
 16K   │ │ │ │ ├── aarch64-ubuntu.dockerfile
 12K   │ │ │ │ ├── README.md
8.0K   │ │ │ │ ├── startup.sh
8.0K   │ │ │ │ ├── run.sh
4.0K   │ │ │ │ └── cron_README.md
 36K   │ │ │ ├─┬ Windows
 24K   │ │ │ │ ├── 0xf_gh_runner_windows_debug.yaml
8.0K   │ │ │ │ └── debloat.ps1
8.0K   │ │ │ └─┬ macOS
4.0K   │ │ │   └── 0xf_gh_runner_macos_debug.yaml
4.0K   │ │ └── GIT.md
188K   │ ├─┬ Linux
 88K   │ │ ├─┬ Debian
 20K   │ │ │ ├── install_bb_tools_x86_64.sh
 20K   │ │ │ ├── install_bb_tools_aarch64.sh
 12K   │ │ │ ├── setup_ssh_x86_64.sh
8.0K   │ │ │ ├── install_ncurses_zig_x86_64.sh
4.0K   │ │ │ ├── install_zig.sh
4.0K   │ │ │ ├── install_node_x86_64.sh
4.0K   │ │ │ ├── install_node_aarch64.sh
4.0K   │ │ │ ├── install_chrome_x86_64.sh
4.0K   │ │ │ ├── install_chrome_aarch64.sh
4.0K   │ │ │ └── bootstrap.sh
 32K   │ │ ├── install_bb_tools.sh
 24K   │ │ ├── install_dev_tools.sh
 12K   │ │ ├── sshd_config_passwordless
 12K   │ │ ├── sshd_config
4.0K   │ │ ├── install_cosmocc.sh
4.0K   │ │ ├── TIPS_TRICKS.md
4.0K   │ │ ├── DAGU_CRON_EXAMPLE.yaml
4.0K   │ │ └── DAGU_CRON.md
 44K   │ ├─┬ WSL
 32K   │ │ ├─┬ Debian
 16K   │ │ │ ├── README.md
8.0K   │ │ │ ├── customize.sh
4.0K   │ │ │ └── starship.toml
8.0K   │ │ └── README.md
 32K   │ ├─┬ Windows
 24K   │ │ ├─┬ scripts
 16K   │ │ │ ├── git_backup_windows.ps1
4.0K   │ │ │ └── README.md
4.0K   │ │ └── TIPS_TRICKS.md
 28K   │ ├─┬ Android
 24K   │ │ └─┬ Termux
 20K   │ │   └── README.md
 24K   │ ├─┬ VMware
 12K   │ │ ├─┬ Parrot_Minimal
8.0K   │ │ │ └── README.md
8.0K   │ │ └─┬ Debian_Minimal
4.0K   │ │   └── README.md
 24K   │ ├─┬ Microsoft
 20K   │ │ └─┬ Azure
 16K   │ │   └── Azure_for_Students.md
 24K   │ ├─┬ Devscripts
8.0K   │ │ ├── github_archive_all.sh
4.0K   │ │ ├── install_zig.sh
4.0K   │ │ ├── install_portable_python_musl.sh
4.0K   │ │ └── install_nmap.sh
 20K   │ ├─┬ Google
 16K   │ │ └─┬ Colab
4.0K   │ │   ├── devsetup.sh
4.0K   │ │   ├── debloat.sh
4.0K   │ │   └── change_hostname.sh
 16K   │ ├─┬ Contabo
 12K   │ │ └── reboot_instance.sh
 16K   │ ├─┬ Amazon
 12K   │ │ └─┬ AWS
8.0K   │ │   └── reboot_instance.sh
 12K   │ ├─┬ Segfault
8.0K   │ │ └── debloat.sh
8.0K   │ └─┬ uBlock
4.0K   │   └── redirects_disable.txt
312K   ├─┬ aki
296K   │ ├─┬ scripts
 76K   │ │ ├── aki_amass_datasources_yaml_checker.sh
 72K   │ │ ├── aki_oneforall_api_py_checker.sh
 68K   │ │ ├── aki_bbot_secrets_yml_checker.sh
 44K   │ │ ├── aki_subfinder_provider_config_yaml_checker.sh
 32K   │ │ └── apikeybeast.py
 12K   │ └── README.md
 28K   ├─┬ resdns
 20K   │ ├── resdns.sh
4.0K   │ └── README.md
 12K   ├── README.md
4.0K   └── LICENSE
```
