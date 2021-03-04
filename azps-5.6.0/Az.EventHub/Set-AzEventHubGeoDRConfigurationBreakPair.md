---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 6e31353724528c4c9096f9475c7093c338ed270f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971101"
---
# <span data-ttu-id="55dff-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="55dff-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="55dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55dff-102">SYNOPSIS</span></span>
<span data-ttu-id="55dff-103">Questa operazione disabilita il ripristino di emergenza e interrompe la replica delle modifiche dallo spazio dei nomi principale a quello secondario</span><span class="sxs-lookup"><span data-stu-id="55dff-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="55dff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55dff-104">SYNTAX</span></span>

### <span data-ttu-id="55dff-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55dff-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55dff-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55dff-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55dff-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55dff-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55dff-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55dff-108">DESCRIPTION</span></span>
<span data-ttu-id="55dff-109">Il cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** disabilita il ripristino di emergenza e interrompe la replica delle modifiche dallo spazio dei nomi primario a quello secondario</span><span class="sxs-lookup"><span data-stu-id="55dff-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="55dff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55dff-110">EXAMPLES</span></span>

### <span data-ttu-id="55dff-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55dff-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="55dff-112">Questa operazione disabilita il ripristino di emergenza e interrompe la replica delle modifiche dallo spazio dei nomi principale a quello secondario</span><span class="sxs-lookup"><span data-stu-id="55dff-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="55dff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55dff-113">PARAMETERS</span></span>

### <span data-ttu-id="55dff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dff-114">-DefaultProfile</span></span>
<span data-ttu-id="55dff-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55dff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55dff-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55dff-116">-InputObject</span></span>
<span data-ttu-id="55dff-117">Oggetto di configurazione GeoDR di Eventhub</span><span class="sxs-lookup"><span data-stu-id="55dff-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="55dff-118">-Name</span><span class="sxs-lookup"><span data-stu-id="55dff-118">-Name</span></span>
<span data-ttu-id="55dff-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="55dff-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="55dff-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55dff-120">-Namespace</span></span>
<span data-ttu-id="55dff-121">Nome spazio dei nomi - Spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="55dff-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="55dff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55dff-122">-PassThru</span></span>
<span data-ttu-id="55dff-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="55dff-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55dff-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="55dff-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55dff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55dff-125">-ResourceGroupName</span></span>
<span data-ttu-id="55dff-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="55dff-126">Resource Group Name</span></span>

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

### <span data-ttu-id="55dff-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55dff-127">-ResourceId</span></span>
<span data-ttu-id="55dff-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="55dff-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="55dff-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55dff-129">-Confirm</span></span>
<span data-ttu-id="55dff-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55dff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55dff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55dff-131">-WhatIf</span></span>
<span data-ttu-id="55dff-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55dff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55dff-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55dff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55dff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dff-134">CommonParameters</span></span>
<span data-ttu-id="55dff-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55dff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dff-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55dff-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dff-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="55dff-137">INPUTS</span></span>

### <span data-ttu-id="55dff-138">System.String</span><span class="sxs-lookup"><span data-stu-id="55dff-138">System.String</span></span>

### <span data-ttu-id="55dff-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="55dff-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="55dff-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55dff-140">OUTPUTS</span></span>

### <span data-ttu-id="55dff-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55dff-141">System.Boolean</span></span>

## <span data-ttu-id="55dff-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="55dff-142">NOTES</span></span>

## <span data-ttu-id="55dff-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55dff-143">RELATED LINKS</span></span>
