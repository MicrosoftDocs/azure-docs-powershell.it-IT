---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202709"
---
# <span data-ttu-id="22e7e-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="22e7e-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="22e7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22e7e-102">SYNOPSIS</span></span>

## <span data-ttu-id="22e7e-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22e7e-103">SYNTAX</span></span>

### <span data-ttu-id="22e7e-104">S1</span><span class="sxs-lookup"><span data-stu-id="22e7e-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e7e-105">S2</span><span class="sxs-lookup"><span data-stu-id="22e7e-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e7e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e7e-106">DESCRIPTION</span></span>
<span data-ttu-id="22e7e-107">Il cmdlet **Reset-AzWebAppPublishingProfile** Reimposta il profilo di pubblicazione per l'app Web specificata.</span><span class="sxs-lookup"><span data-stu-id="22e7e-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="22e7e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22e7e-108">EXAMPLES</span></span>

### <span data-ttu-id="22e7e-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22e7e-109">Example 1</span></span>

<span data-ttu-id="22e7e-110">L'esempio seguente reimposta il profilo di pubblicazione per l'app Web IpRule associato al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22e7e-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="22e7e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22e7e-111">PARAMETERS</span></span>

### <span data-ttu-id="22e7e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e7e-112">-DefaultProfile</span></span>
<span data-ttu-id="22e7e-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22e7e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e7e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="22e7e-114">-Name</span></span>
<span data-ttu-id="22e7e-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="22e7e-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e7e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e7e-116">-ResourceGroupName</span></span>
<span data-ttu-id="22e7e-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="22e7e-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e7e-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="22e7e-118">-WebApp</span></span>
<span data-ttu-id="22e7e-119">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="22e7e-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e7e-120">CommonParameters</span></span>
<span data-ttu-id="22e7e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e7e-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e7e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e7e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22e7e-123">INPUTS</span></span>

### <span data-ttu-id="22e7e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="22e7e-124">System.String</span></span>

### <span data-ttu-id="22e7e-125">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="22e7e-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="22e7e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22e7e-126">OUTPUTS</span></span>

### <span data-ttu-id="22e7e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="22e7e-127">System.String</span></span>

## <span data-ttu-id="22e7e-128">Note</span><span class="sxs-lookup"><span data-stu-id="22e7e-128">NOTES</span></span>

## <span data-ttu-id="22e7e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22e7e-129">RELATED LINKS</span></span>
