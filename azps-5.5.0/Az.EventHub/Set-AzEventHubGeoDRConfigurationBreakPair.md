---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200358"
---
# <span data-ttu-id="6ad6b-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="6ad6b-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="6ad6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad6b-103">Questa operazione disabilita il ripristino di emergenza e interrompe la replica delle modifiche apportate dagli spazi dei nomi principali a secondari</span><span class="sxs-lookup"><span data-stu-id="6ad6b-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6ad6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ad6b-104">SYNTAX</span></span>

### <span data-ttu-id="6ad6b-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ad6b-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad6b-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ad6b-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad6b-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad6b-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad6b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ad6b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad6b-109">Il cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** disabilita il ripristino di emergenza e interrompe la replica delle modifiche dallo spazio dei nomi primario a quello secondario</span><span class="sxs-lookup"><span data-stu-id="6ad6b-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6ad6b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ad6b-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad6b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ad6b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="6ad6b-112">Questa operazione disabilita il ripristino di emergenza e interrompe la replica delle modifiche apportate dagli spazi dei nomi principali a secondari</span><span class="sxs-lookup"><span data-stu-id="6ad6b-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="6ad6b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad6b-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad6b-114">-DefaultProfile</span></span>
<span data-ttu-id="6ad6b-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad6b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ad6b-116">-InputObject</span></span>
<span data-ttu-id="6ad6b-117">Oggetto di configurazione GeoDR di Eventhub</span><span class="sxs-lookup"><span data-stu-id="6ad6b-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="6ad6b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6ad6b-118">-Name</span></span>
<span data-ttu-id="6ad6b-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="6ad6b-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="6ad6b-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ad6b-120">-Namespace</span></span>
<span data-ttu-id="6ad6b-121">Nome spazio dei nomi - Spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="6ad6b-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="6ad6b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ad6b-122">-PassThru</span></span>
<span data-ttu-id="6ad6b-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6ad6b-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ad6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ad6b-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6ad6b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6ad6b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad6b-127">-ResourceId</span></span>
<span data-ttu-id="6ad6b-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad6b-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="6ad6b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad6b-129">-Confirm</span></span>
<span data-ttu-id="6ad6b-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad6b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad6b-131">-WhatIf</span></span>
<span data-ttu-id="6ad6b-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad6b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad6b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad6b-134">CommonParameters</span></span>
<span data-ttu-id="6ad6b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad6b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad6b-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad6b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad6b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ad6b-137">INPUTS</span></span>

### <span data-ttu-id="6ad6b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6ad6b-138">System.String</span></span>

### <span data-ttu-id="6ad6b-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="6ad6b-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="6ad6b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ad6b-140">OUTPUTS</span></span>

### <span data-ttu-id="6ad6b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ad6b-141">System.Boolean</span></span>

## <span data-ttu-id="6ad6b-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ad6b-142">NOTES</span></span>

## <span data-ttu-id="6ad6b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ad6b-143">RELATED LINKS</span></span>
