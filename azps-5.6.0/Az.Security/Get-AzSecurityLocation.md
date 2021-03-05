---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: b835113b07fb2295193b89fd817ba82ceca71655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995957"
---
# <span data-ttu-id="76f01-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="76f01-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="76f01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f01-102">SYNOPSIS</span></span>
<span data-ttu-id="76f01-103">Ottiene la posizione in cui il Centro sicurezza di Azure salverà automaticamente i dati per la sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="76f01-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="76f01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76f01-104">SYNTAX</span></span>

### <span data-ttu-id="76f01-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76f01-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f01-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="76f01-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f01-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="76f01-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f01-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76f01-108">DESCRIPTION</span></span>
<span data-ttu-id="76f01-109">Il Centro sicurezza di Azure deciderà automaticamente una posizione in cui salvare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="76f01-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="76f01-110">Usare questo cmdlet per individuare la posizione.</span><span class="sxs-lookup"><span data-stu-id="76f01-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="76f01-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76f01-111">EXAMPLES</span></span>

### <span data-ttu-id="76f01-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76f01-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="76f01-113">Ottiene la posizione in cui il Centro sicurezza di Azure salva i dati di sicurezza calcolati.</span><span class="sxs-lookup"><span data-stu-id="76f01-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="76f01-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f01-114">PARAMETERS</span></span>

### <span data-ttu-id="76f01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f01-115">-DefaultProfile</span></span>
<span data-ttu-id="76f01-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f01-117">-Name</span><span class="sxs-lookup"><span data-stu-id="76f01-117">-Name</span></span>
<span data-ttu-id="76f01-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="76f01-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f01-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76f01-119">-ResourceId</span></span>
<span data-ttu-id="76f01-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="76f01-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f01-121">CommonParameters</span></span>
<span data-ttu-id="76f01-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f01-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76f01-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f01-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="76f01-124">INPUTS</span></span>

### <span data-ttu-id="76f01-125">System.String</span><span class="sxs-lookup"><span data-stu-id="76f01-125">System.String</span></span>

## <span data-ttu-id="76f01-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76f01-126">OUTPUTS</span></span>

### <span data-ttu-id="76f01-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="76f01-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="76f01-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="76f01-128">NOTES</span></span>

## <span data-ttu-id="76f01-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76f01-129">RELATED LINKS</span></span>
