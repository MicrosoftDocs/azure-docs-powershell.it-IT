---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188256"
---
# <span data-ttu-id="2d582-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="2d582-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="2d582-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d582-102">SYNOPSIS</span></span>
<span data-ttu-id="2d582-103">Ottiene un elenco di gruppi VM/Server di controllo applicazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2d582-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2d582-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d582-104">SYNTAX</span></span>

### <span data-ttu-id="2d582-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2d582-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d582-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d582-106">DESCRIPTION</span></span>
<span data-ttu-id="2d582-107">I controlli applicativi adattivi vengono calcolati automaticamente da Azure Security Center, usa questo cmdlet per ottenere un elenco delle risorse di controllo dell'applicazione adattiva nell'ambito di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2d582-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="2d582-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d582-108">EXAMPLES</span></span>

### <span data-ttu-id="2d582-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d582-109">Example 1</span></span>
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
<span data-ttu-id="2d582-110">Ottiene un elenco di gruppi VM/Server di controllo applicazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2d582-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2d582-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d582-111">PARAMETERS</span></span>

### <span data-ttu-id="2d582-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d582-112">-DefaultProfile</span></span>
<span data-ttu-id="2d582-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d582-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d582-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d582-114">-SubscriptionId</span></span>
<span data-ttu-id="2d582-115">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d582-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="2d582-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="2d582-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="2d582-117">Includere le regole dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2d582-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="2d582-118">-Riepilogo</span><span class="sxs-lookup"><span data-stu-id="2d582-118">-Summary</span></span>
<span data-ttu-id="2d582-119">Restituire l'output in un modulo riepilogato.</span><span class="sxs-lookup"><span data-stu-id="2d582-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="2d582-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d582-120">CommonParameters</span></span>
<span data-ttu-id="2d582-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d582-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d582-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d582-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d582-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d582-123">INPUTS</span></span>

### <span data-ttu-id="2d582-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2d582-124">System.String</span></span>

### <span data-ttu-id="2d582-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d582-125">System.Boolean</span></span>

## <span data-ttu-id="2d582-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d582-126">OUTPUTS</span></span>

### <span data-ttu-id="2d582-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="2d582-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="2d582-128">Note</span><span class="sxs-lookup"><span data-stu-id="2d582-128">NOTES</span></span>

## <span data-ttu-id="2d582-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d582-129">RELATED LINKS</span></span>