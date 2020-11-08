---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032759"
---
# <span data-ttu-id="b9780-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b9780-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="b9780-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9780-102">SYNOPSIS</span></span>

## <span data-ttu-id="b9780-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9780-103">SYNTAX</span></span>

### <span data-ttu-id="b9780-104">S1</span><span class="sxs-lookup"><span data-stu-id="b9780-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9780-105">S2</span><span class="sxs-lookup"><span data-stu-id="b9780-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9780-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9780-106">DESCRIPTION</span></span>
<span data-ttu-id="b9780-107">Il cmdlet **Reset-AzWebAppPublishingProfile** Reimposta il profilo di pubblicazione per l'app Web specificata.</span><span class="sxs-lookup"><span data-stu-id="b9780-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="b9780-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9780-108">EXAMPLES</span></span>

### <span data-ttu-id="b9780-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9780-109">Example 1</span></span>

<span data-ttu-id="b9780-110">L'esempio seguente reimposta il profilo di pubblicazione per l'app Web IpRule associato al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9780-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="b9780-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9780-111">PARAMETERS</span></span>

### <span data-ttu-id="b9780-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9780-112">-DefaultProfile</span></span>
<span data-ttu-id="b9780-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9780-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9780-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9780-114">-Name</span></span>
<span data-ttu-id="b9780-115">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b9780-115">WebApp Name</span></span>

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

### <span data-ttu-id="b9780-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9780-116">-ResourceGroupName</span></span>
<span data-ttu-id="b9780-117">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b9780-117">Resource Group Name</span></span>

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

### <span data-ttu-id="b9780-118">-Web App</span><span class="sxs-lookup"><span data-stu-id="b9780-118">-WebApp</span></span>
<span data-ttu-id="b9780-119">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="b9780-119">WebApp Object</span></span>

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

### <span data-ttu-id="b9780-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9780-120">CommonParameters</span></span>
<span data-ttu-id="b9780-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9780-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9780-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9780-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9780-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9780-123">INPUTS</span></span>

### <span data-ttu-id="b9780-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b9780-124">System.String</span></span>

### <span data-ttu-id="b9780-125">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b9780-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b9780-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9780-126">OUTPUTS</span></span>

### <span data-ttu-id="b9780-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9780-127">System.String</span></span>

## <span data-ttu-id="b9780-128">Note</span><span class="sxs-lookup"><span data-stu-id="b9780-128">NOTES</span></span>

## <span data-ttu-id="b9780-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9780-129">RELATED LINKS</span></span>
