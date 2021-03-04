---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: d68fe2005f827d55b57ecedb7e21fd11b0cc9978
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986046"
---
# <span data-ttu-id="af277-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="af277-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="af277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af277-102">SYNOPSIS</span></span>
<span data-ttu-id="af277-103">Richiama il failover di GEO DR e riconfigura l'alias in modo che punti allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="af277-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="af277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af277-104">SYNTAX</span></span>

### <span data-ttu-id="af277-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af277-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af277-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af277-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af277-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af277-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af277-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af277-108">DESCRIPTION</span></span>
<span data-ttu-id="af277-109">Il cmdlet **Set-AzEventHubGeoDRConfigurationFailOver** richiama il failover GEO DR e riconfigura l'alias in modo che punti allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="af277-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="af277-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af277-110">EXAMPLES</span></span>

### <span data-ttu-id="af277-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af277-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="af277-112">Richiama il failover sull'alias "SampleDRConfigName", riconfigura e punta allo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="af277-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="af277-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af277-113">PARAMETERS</span></span>

### <span data-ttu-id="af277-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af277-114">-DefaultProfile</span></span>
<span data-ttu-id="af277-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af277-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af277-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af277-116">-InputObject</span></span>
<span data-ttu-id="af277-117">Oggetto di configurazione GeoDR di Eventhub</span><span class="sxs-lookup"><span data-stu-id="af277-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af277-118">-Name</span><span class="sxs-lookup"><span data-stu-id="af277-118">-Name</span></span>
<span data-ttu-id="af277-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="af277-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af277-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af277-120">-Namespace</span></span>
<span data-ttu-id="af277-121">Nome spazio dei nomi - Spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="af277-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af277-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af277-122">-PassThru</span></span>
<span data-ttu-id="af277-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="af277-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af277-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="af277-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af277-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af277-125">-ResourceGroupName</span></span>
<span data-ttu-id="af277-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af277-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af277-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af277-127">-ResourceId</span></span>
<span data-ttu-id="af277-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="af277-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af277-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af277-129">-Confirm</span></span>
<span data-ttu-id="af277-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af277-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af277-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af277-131">-WhatIf</span></span>
<span data-ttu-id="af277-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af277-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af277-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af277-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af277-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af277-134">CommonParameters</span></span>
<span data-ttu-id="af277-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af277-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af277-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af277-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af277-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="af277-137">INPUTS</span></span>

### <span data-ttu-id="af277-138">System.String</span><span class="sxs-lookup"><span data-stu-id="af277-138">System.String</span></span>

### <span data-ttu-id="af277-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="af277-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="af277-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af277-140">OUTPUTS</span></span>

### <span data-ttu-id="af277-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af277-141">System.Boolean</span></span>

## <span data-ttu-id="af277-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="af277-142">NOTES</span></span>

## <span data-ttu-id="af277-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af277-143">RELATED LINKS</span></span>
