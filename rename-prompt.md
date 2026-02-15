You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/95585b72781cff251800a99a941eacfc.css",
    "context": {
      "path": "css/95585b72781cff251800a99a941eacfc.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/004ee7731c6f6aa2cecd0e5dd8760bbc.webp",
    "context": {
      "refs": [
        {
          "alt": "Workplaces",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/05bfa753e44b508c12942b83d87f26dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/066f889c3e02303d2881c8adf74897e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0872859b50f1ae5ab63656d9210c526f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ae841aff9cbcbe40682374c334ec2aa.webp",
    "context": {
      "refs": [
        {
          "alt": "GLOBAL WITH LOCAL CONNECT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0dcf46e53fb6d04f6664f4f2677f4638.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10e28764f83acf6614aa95d8c83955ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1209d73b2c89cbc19975fff5101fe058.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/122851b4e8818a6f22ee679f977fbb98.webp",
    "context": {
      "refs": [
        {
          "alt": "WORKPLACE DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/13031b068c9191451c1bfe453ba2a78c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/17ac578ca98d691bc5796ea70d530768.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b20d4b4c808e654f572bbff943756b7.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1df4ebe083f0a350b5a20b657a15b6d8.webp",
    "context": {
      "refs": [
        {
          "alt": "THEMED INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/204adf967c116de2d0bd00e3c95a5f16.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22b3c07d89bf9dbe05e12ef7bc966bde.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/235828c3502e62f34786d75455fa7238.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23a3a3037ec59f06f280b7d50188a750.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/259200e97f3110a793288592df272170.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25f63f99cb93bf1a0a4a279149f971e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2797a78898d77b7f9ae523afef2ab2de.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28084aed4c73c1e69d7f7236bdfda5f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2beff1073188658993e1e89d959b45b6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e9e319912173ddfe09140360e727c9d.webp",
    "context": {
      "refs": [
        {
          "alt": "EXPERIENTIAL WORKPLACES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ebd2e9643518b96d1c449480ca72792.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30345f465edcd67355e8bca0406db43b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/370941c51e5d58a48ef95bc7af6ed760.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38182eb05d120d1a4b364f117e87fbf8.webp",
    "context": {
      "refs": [
        {
          "alt": "RESIDENTIAL DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a0619f9636852ea282e1a51ca08f7ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b163250f54ce0c0d8cb9e59a9786a93.webp",
    "context": {
      "refs": [
        {
          "alt": "RETAIL DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/434f10384d132492841539134d565cc4.webp",
    "context": {
      "refs": [
        {
          "alt": "ARCHITECTURE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/468cacab769e10cc1d39e918174bc3e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a938b773d5757c09a15e1842aff62be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bc08765995f80e7a8d94ec917179645.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d34a885ba8862bfe4ee54c0f86fc17b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a0f8c6e9295416083d2de8393ae1d07.webp",
    "context": {
      "refs": [
        {
          "alt": "DESIGN RESEARCH",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5fd454849324f4327c752beb0269fb35.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6004c35ec451818119405c9a8a42d824.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66fe9b4c70d725bb6ce5fba6dde2db70.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68592210ae6ff708bcf8742320a8574e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/696ff0761a02df4fa8f56ccb3f231dbb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ab221e8cd5fe4ce0572e9cff394d187.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6aca7a4678beefc8aff50a7c0b8de836.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f4aab40819f60751c7dea159b396108.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fd96e32b14703fe971aa0d0426f4b0e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/705573464f2cf7aed0407572b9d2b493.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7398c9f3122fea57d67bc0757ba96a53.webp",
    "context": {
      "refs": [
        {
          "alt": "WORKPLACE DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7532839abee63eb4d0f1ee0d14497f6f.webp",
    "context": {
      "refs": [
        {
          "alt": "URBAN ECONOMICS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/772085d091de5c1c4cc064e721e11cb1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7916c3c35587f53fb3a7483209438f6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8190345649c0924506b7d72e5809368f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/828425ecb512021354be840f18d02388.webp",
    "context": {
      "refs": [
        {
          "alt": "MODERN WORKSPACES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/832de33b8e23c9b42b543c9f985baef9.webp",
    "context": {
      "refs": [
        {
          "alt": "Smart offices",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/837318f406d123f67c162fe9e29f6f8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/863aa5936ef51e700214905ceb732e6b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8bdc9ff902700b868c0aad16b5917017.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/969f3d1294b8c66a62dbcd4c6895693c.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9ff4b20cb4037edef37ac40e2184825c.webp",
    "context": {
      "refs": [
        {
          "alt": "CORPORATE INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a031279da05b62e495fe98e7aa7650d2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a114c88560d432277fd4b9e5173e2d5d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5301e29a738eab34c1b81e746f47d25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a666b920a50b0f7dfd36015871024b37.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a84310620d09bf12c8c10668580ae6cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a94151bde07dc308fba2a3289c3f4c7b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b233ecb9ee579659f34ea9093e0b0f95.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b957fbb954c7920ac78408c52b94f859.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9ae9acf2a25f394d1320f05904bd53a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdf2e6f6bc5631df21db05e60ab63f8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6ba931f2271de4a705fb48fff50ffe7.webp",
    "context": {
      "refs": [
        {
          "alt": "THEMED INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c83ee86156178c1078a24b828328e5d6.webp",
    "context": {
      "refs": [
        {
          "alt": "MODERN WORKSPACES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c936333b0490a801c1a5ef3a4b4ec5f0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca348e520350cb5dac5f530c1f8305fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cccfbf33f769f693fc2247e5e123786f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cda2e238ea4299db3ca40cf26527b9c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ced085924c6c034e0d2fa43d18551db6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d03576ab83f3d1970b0f5c01533bfd72.webp",
    "context": {
      "refs": [
        {
          "alt": "RESIDENTIAL INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0a27eda6c789b3491e8bc3f6fe761be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2ea77832257251e0978dde6cb7c9114.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5da45732658f94450200223c08e7b4e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e082f43a629e1d302fd0ae9b30420a84.webp",
    "context": {
      "refs": [
        {
          "alt": "GLOBAL WITH LOCAL CONNECT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e22bf1f3dbb969be7be656244c78f95a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e85e79052a665bbadbe8d6f75b4047f2.webp",
    "context": {
      "refs": [
        {
          "alt": "CORPORATE INTERIOR DESIGN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e92c0c994e674e0b40b12de4818e214c.webp",
    "context": {
      "refs": [
        {
          "alt": "Designtude",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb90aaa4c9dfb3acbd5b2c5a0a40abf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee1178bf9c9ca53f9c24303687ce8839.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2d6a7d38a224a49de7e11d45f9eeb15.webp",
    "context": {
      "refs": [
        {
          "alt": "Designtude Studio",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f36f63ebcb91f08764c2ff5a26c46e3f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Interior Design, Architecture, Workspace, Corporate Services",
      "first_heading": "Reception themed as fashion high street"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e734a79111d3ae5022fadd97f4b4570.js",
    "context": {
      "path": "js/3e734a79111d3ae5022fadd97f4b4570.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js",
    "context": {
      "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "thoughts.html",
    "context": {
      "title": "Interior Design, Architecture, Workspace, Corporate Services",
      "first_heading": "THOUGHTS"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.