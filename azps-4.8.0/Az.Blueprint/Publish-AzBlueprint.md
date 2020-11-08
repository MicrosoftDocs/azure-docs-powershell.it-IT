---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031358"
---
# <span data-ttu-id="7e094-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e094-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="7e094-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e094-102">SYNOPSIS</span></span>
<span data-ttu-id="7e094-103">Pubblicare una nuova versione di un modello.</span><span class="sxs-lookup"><span data-stu-id="7e094-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="7e094-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e094-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e094-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e094-105">DESCRIPTION</span></span>
<span data-ttu-id="7e094-106">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e094-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7e094-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e094-107">EXAMPLES</span></span>

### <span data-ttu-id="7e094-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e094-108">Example 1</span></span>
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

<span data-ttu-id="7e094-109">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e094-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7e094-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e094-110">PARAMETERS</span></span>

### <span data-ttu-id="7e094-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="7e094-111">-Blueprint</span></span>
<span data-ttu-id="7e094-112">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e094-112">Blueprint object.</span></span>

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

### <span data-ttu-id="7e094-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="7e094-113">-ChangeNote</span></span>
<span data-ttu-id="7e094-114">Note per descrivere il contenuto di questa versione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e094-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="7e094-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e094-115">-DefaultProfile</span></span>
<span data-ttu-id="7e094-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e094-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e094-117">-Versione</span><span class="sxs-lookup"><span data-stu-id="7e094-117">-Version</span></span>
<span data-ttu-id="7e094-118">Versione per la definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="7e094-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="7e094-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e094-119">-Confirm</span></span>
<span data-ttu-id="7e094-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e094-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e094-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e094-121">-WhatIf</span></span>
<span data-ttu-id="7e094-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e094-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e094-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e094-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e094-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e094-124">CommonParameters</span></span>
<span data-ttu-id="7e094-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e094-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e094-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e094-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e094-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e094-127">INPUTS</span></span>

### <span data-ttu-id="7e094-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7e094-128">System.String</span></span>

### <span data-ttu-id="7e094-129">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e094-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="7e094-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e094-130">OUTPUTS</span></span>

### <span data-ttu-id="7e094-131">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e094-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="7e094-132">Note</span><span class="sxs-lookup"><span data-stu-id="7e094-132">NOTES</span></span>

## <span data-ttu-id="7e094-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e094-133">RELATED LINKS</span></span>
