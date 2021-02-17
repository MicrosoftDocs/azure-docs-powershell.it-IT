---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191222"
---
# <span data-ttu-id="7450c-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="7450c-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="7450c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7450c-102">SYNOPSIS</span></span>
<span data-ttu-id="7450c-103">Ottiene un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7450c-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="7450c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7450c-104">SYNTAX</span></span>

### <span data-ttu-id="7450c-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7450c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7450c-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7450c-106">DESCRIPTION</span></span>
<span data-ttu-id="7450c-107">I controlli adattivi delle applicazioni vengono calcolati automaticamente dal Centro sicurezza e usano questo cmdlet per ottenere un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7450c-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="7450c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7450c-108">EXAMPLES</span></span>

### <span data-ttu-id="7450c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7450c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="7450c-110">Ottiene un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7450c-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="7450c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7450c-111">PARAMETERS</span></span>

### <span data-ttu-id="7450c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7450c-112">-DefaultProfile</span></span>
<span data-ttu-id="7450c-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7450c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7450c-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="7450c-114">-AscLocation</span></span>
<span data-ttu-id="7450c-115">Posizione in cui asc archivia i dati della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7450c-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="7450c-116">possono essere recuperate da Ottieni posizioni.</span><span class="sxs-lookup"><span data-stu-id="7450c-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450c-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7450c-117">-GroupName</span></span>
<span data-ttu-id="7450c-118">Nome di un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7450c-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7450c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7450c-119">-SubscriptionId</span></span>
<span data-ttu-id="7450c-120">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="7450c-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="7450c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7450c-121">CommonParameters</span></span>
<span data-ttu-id="7450c-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7450c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7450c-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7450c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7450c-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="7450c-124">INPUTS</span></span>

### <span data-ttu-id="7450c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7450c-125">System.String</span></span>

## <span data-ttu-id="7450c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7450c-126">OUTPUTS</span></span>

### <span data-ttu-id="7450c-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplication Più.PsSecurityAdaptiveApplicationApplication</span><span class="sxs-lookup"><span data-stu-id="7450c-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="7450c-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="7450c-128">NOTES</span></span>

## <span data-ttu-id="7450c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7450c-129">RELATED LINKS</span></span>