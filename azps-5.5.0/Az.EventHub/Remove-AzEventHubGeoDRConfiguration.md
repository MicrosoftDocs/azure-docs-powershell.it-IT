---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204098"
---
# <span data-ttu-id="0c361-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c361-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="0c361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c361-102">SYNOPSIS</span></span>
<span data-ttu-id="0c361-103">Elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="0c361-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0c361-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c361-104">SYNTAX</span></span>

### <span data-ttu-id="0c361-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c361-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c361-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c361-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c361-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c361-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c361-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c361-108">DESCRIPTION</span></span>
<span data-ttu-id="0c361-109">Il cmdlet **Remove-AzEventHubGeoDRConfiguration** elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="0c361-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0c361-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c361-110">EXAMPLES</span></span>

### <span data-ttu-id="0c361-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c361-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="0c361-112">Elimina un alias (configurazione di ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="0c361-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="0c361-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c361-113">PARAMETERS</span></span>

### <span data-ttu-id="0c361-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c361-114">-AsJob</span></span>
<span data-ttu-id="0c361-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0c361-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c361-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c361-116">-DefaultProfile</span></span>
<span data-ttu-id="0c361-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c361-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c361-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c361-118">-InputObject</span></span>
<span data-ttu-id="0c361-119">Oggetto di configurazione GeoDR di Eventhub</span><span class="sxs-lookup"><span data-stu-id="0c361-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="0c361-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c361-120">-Name</span></span>
<span data-ttu-id="0c361-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="0c361-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="0c361-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c361-122">-Namespace</span></span>
<span data-ttu-id="0c361-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c361-123">Namespace Name</span></span>

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

### <span data-ttu-id="0c361-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c361-124">-PassThru</span></span>
<span data-ttu-id="0c361-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0c361-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c361-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0c361-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c361-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c361-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c361-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0c361-128">Resource Group Name</span></span>

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

### <span data-ttu-id="0c361-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c361-129">-ResourceId</span></span>
<span data-ttu-id="0c361-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c361-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="0c361-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c361-131">-Confirm</span></span>
<span data-ttu-id="0c361-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c361-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c361-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c361-133">-WhatIf</span></span>
<span data-ttu-id="0c361-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c361-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c361-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c361-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c361-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c361-136">CommonParameters</span></span>
<span data-ttu-id="0c361-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c361-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c361-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c361-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c361-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c361-139">INPUTS</span></span>

### <span data-ttu-id="0c361-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0c361-140">System.String</span></span>

### <span data-ttu-id="0c361-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0c361-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="0c361-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c361-142">OUTPUTS</span></span>

### <span data-ttu-id="0c361-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c361-143">System.Boolean</span></span>

## <span data-ttu-id="0c361-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c361-144">NOTES</span></span>

## <span data-ttu-id="0c361-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c361-145">RELATED LINKS</span></span>
