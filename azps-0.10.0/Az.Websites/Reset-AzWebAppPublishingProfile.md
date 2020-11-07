---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861866"
---
# <span data-ttu-id="7df13-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7df13-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="7df13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7df13-102">SYNOPSIS</span></span>

## <span data-ttu-id="7df13-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7df13-103">SYNTAX</span></span>

### <span data-ttu-id="7df13-104">S1</span><span class="sxs-lookup"><span data-stu-id="7df13-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7df13-105">S2</span><span class="sxs-lookup"><span data-stu-id="7df13-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7df13-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7df13-106">DESCRIPTION</span></span>
<span data-ttu-id="7df13-107">Il cmdlet **Reset-AzWebAppPublishingProfile** Reimposta il profilo di pubblicazione per l'app Web specificata.</span><span class="sxs-lookup"><span data-stu-id="7df13-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="7df13-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7df13-108">EXAMPLES</span></span>

### <span data-ttu-id="7df13-109">1:</span><span class="sxs-lookup"><span data-stu-id="7df13-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="7df13-110">Questo comando Reimposta il profilo di pubblicazione per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="7df13-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7df13-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7df13-111">PARAMETERS</span></span>

### <span data-ttu-id="7df13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df13-112">-DefaultProfile</span></span>
<span data-ttu-id="7df13-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7df13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df13-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7df13-114">-Name</span></span>
<span data-ttu-id="7df13-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="7df13-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df13-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df13-116">-ResourceGroupName</span></span>
<span data-ttu-id="7df13-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7df13-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df13-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="7df13-118">-WebApp</span></span>
<span data-ttu-id="7df13-119">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="7df13-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7df13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df13-120">CommonParameters</span></span>
<span data-ttu-id="7df13-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df13-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df13-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df13-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7df13-123">INPUTS</span></span>

### <span data-ttu-id="7df13-124">Sito</span><span class="sxs-lookup"><span data-stu-id="7df13-124">Site</span></span>
<span data-ttu-id="7df13-125">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7df13-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7df13-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7df13-126">OUTPUTS</span></span>

## <span data-ttu-id="7df13-127">Note</span><span class="sxs-lookup"><span data-stu-id="7df13-127">NOTES</span></span>

## <span data-ttu-id="7df13-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7df13-128">RELATED LINKS</span></span>

