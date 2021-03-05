---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: bc1ec66846037a7081af85809f2187b5d35aecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010830"
---
# <span data-ttu-id="95309-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="95309-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="95309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95309-102">SYNOPSIS</span></span>
<span data-ttu-id="95309-103">Pubblica una nuova versione di una progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="95309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95309-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95309-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="95309-105">DESCRIPTION</span></span>
<span data-ttu-id="95309-106">Pubblicare una nuova versione di una definizione di progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="95309-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95309-107">EXAMPLES</span></span>

### <span data-ttu-id="95309-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95309-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="95309-109">Pubblicare una nuova versione di una definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="95309-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95309-110">PARAMETERS</span></span>

### <span data-ttu-id="95309-111">-Progetto</span><span class="sxs-lookup"><span data-stu-id="95309-111">-Blueprint</span></span>
<span data-ttu-id="95309-112">Oggetto progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="95309-113">-ChangeNote</span></span>
<span data-ttu-id="95309-114">Note per descrivere il contenuto di questa versione del progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-114">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95309-115">-DefaultProfile</span></span>
<span data-ttu-id="95309-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95309-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95309-117">-Version</span><span class="sxs-lookup"><span data-stu-id="95309-117">-Version</span></span>
<span data-ttu-id="95309-118">Versione per la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="95309-118">Version for the blueprint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95309-119">-Confirm</span></span>
<span data-ttu-id="95309-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95309-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95309-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95309-121">-WhatIf</span></span>
<span data-ttu-id="95309-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95309-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95309-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95309-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95309-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95309-124">CommonParameters</span></span>
<span data-ttu-id="95309-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95309-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95309-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95309-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95309-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="95309-127">INPUTS</span></span>

### <span data-ttu-id="95309-128">System.String</span><span class="sxs-lookup"><span data-stu-id="95309-128">System.String</span></span>

### <span data-ttu-id="95309-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="95309-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="95309-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95309-130">OUTPUTS</span></span>

### <span data-ttu-id="95309-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="95309-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="95309-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="95309-132">NOTES</span></span>

## <span data-ttu-id="95309-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95309-133">RELATED LINKS</span></span>
