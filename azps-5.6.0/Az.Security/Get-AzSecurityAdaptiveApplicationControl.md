---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: ec35083cf4495d0bf262d841563f0dc4100dcdc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974350"
---
# <span data-ttu-id="650e3-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="650e3-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="650e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650e3-102">SYNOPSIS</span></span>
<span data-ttu-id="650e3-103">Ottiene un elenco di gruppi di server/vm di controllo applicazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="650e3-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="650e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="650e3-104">SYNTAX</span></span>

### <span data-ttu-id="650e3-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="650e3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="650e3-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="650e3-106">DESCRIPTION</span></span>
<span data-ttu-id="650e3-107">I controlli adattivi delle applicazioni vengono calcolati automaticamente dal Centro sicurezza e conformità di Azure. Usare questo cmdlet per ottenere un elenco di risorse controlli adattivi per le applicazioni nell'ambito di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="650e3-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="650e3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="650e3-108">EXAMPLES</span></span>

### <span data-ttu-id="650e3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="650e3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="650e3-110">Ottiene un elenco di gruppi di server/vm di controllo applicazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="650e3-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="650e3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650e3-111">PARAMETERS</span></span>

### <span data-ttu-id="650e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650e3-112">-DefaultProfile</span></span>
<span data-ttu-id="650e3-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="650e3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="650e3-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="650e3-114">-SubscriptionId</span></span>
<span data-ttu-id="650e3-115">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="650e3-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650e3-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="650e3-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="650e3-117">Includere le regole dei criteri.</span><span class="sxs-lookup"><span data-stu-id="650e3-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650e3-118">-Summary</span><span class="sxs-lookup"><span data-stu-id="650e3-118">-Summary</span></span>
<span data-ttu-id="650e3-119">Restituisce l'output in formato riepilogato.</span><span class="sxs-lookup"><span data-stu-id="650e3-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650e3-120">CommonParameters</span></span>
<span data-ttu-id="650e3-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650e3-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="650e3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650e3-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="650e3-123">INPUTS</span></span>

### <span data-ttu-id="650e3-124">System.String</span><span class="sxs-lookup"><span data-stu-id="650e3-124">System.String</span></span>

### <span data-ttu-id="650e3-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="650e3-125">System.Boolean</span></span>

## <span data-ttu-id="650e3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="650e3-126">OUTPUTS</span></span>

### <span data-ttu-id="650e3-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplication Più.PsSecurityAdaptiveApplicationApplication</span><span class="sxs-lookup"><span data-stu-id="650e3-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="650e3-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="650e3-128">NOTES</span></span>

## <span data-ttu-id="650e3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="650e3-129">RELATED LINKS</span></span>
