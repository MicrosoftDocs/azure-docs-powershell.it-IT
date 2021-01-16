---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344452"
---
# <span data-ttu-id="34e9c-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="34e9c-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="34e9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="34e9c-103">Ottiene un gruppo di VM/Server di controllo applicazione.</span><span class="sxs-lookup"><span data-stu-id="34e9c-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="34e9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e9c-104">SYNTAX</span></span>

### <span data-ttu-id="34e9c-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34e9c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e9c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e9c-106">DESCRIPTION</span></span>
<span data-ttu-id="34e9c-107">I controlli di applicazione adattiva vengono calcolati automaticamente da Azure Security Center, usa questo cmdlet per ottenere un gruppo di VM/Server di controllo applicazione.</span><span class="sxs-lookup"><span data-stu-id="34e9c-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="34e9c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e9c-108">EXAMPLES</span></span>

### <span data-ttu-id="34e9c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34e9c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="34e9c-110">Ottiene un gruppo di VM/Server di controllo applicazione.</span><span class="sxs-lookup"><span data-stu-id="34e9c-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="34e9c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e9c-111">PARAMETERS</span></span>

### <span data-ttu-id="34e9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e9c-112">-DefaultProfile</span></span>
<span data-ttu-id="34e9c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34e9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34e9c-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="34e9c-114">-AscLocation</span></span>
<span data-ttu-id="34e9c-115">Posizione in cui ASC archivia i dati dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="34e9c-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="34e9c-116">può essere recuperato da Get locations.</span><span class="sxs-lookup"><span data-stu-id="34e9c-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="34e9c-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="34e9c-117">-GroupName</span></span>
<span data-ttu-id="34e9c-118">Nome di un gruppo di VM/Server di controllo applicazione.</span><span class="sxs-lookup"><span data-stu-id="34e9c-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="34e9c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34e9c-119">-SubscriptionId</span></span>
<span data-ttu-id="34e9c-120">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e9c-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="34e9c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e9c-121">CommonParameters</span></span>
<span data-ttu-id="34e9c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e9c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e9c-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e9c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e9c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34e9c-124">INPUTS</span></span>

### <span data-ttu-id="34e9c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="34e9c-125">System.String</span></span>

## <span data-ttu-id="34e9c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e9c-126">OUTPUTS</span></span>

### <span data-ttu-id="34e9c-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="34e9c-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="34e9c-128">Note</span><span class="sxs-lookup"><span data-stu-id="34e9c-128">NOTES</span></span>

## <span data-ttu-id="34e9c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e9c-129">RELATED LINKS</span></span>