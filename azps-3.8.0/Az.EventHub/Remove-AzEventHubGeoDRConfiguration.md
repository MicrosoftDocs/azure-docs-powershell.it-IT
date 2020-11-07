---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864491"
---
# <span data-ttu-id="356e7-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e7-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="356e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="356e7-102">SYNOPSIS</span></span>
<span data-ttu-id="356e7-103">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="356e7-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="356e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="356e7-104">SYNTAX</span></span>

### <span data-ttu-id="356e7-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="356e7-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356e7-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="356e7-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356e7-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="356e7-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="356e7-108">DESCRIPTION</span></span>
<span data-ttu-id="356e7-109">Il cmdlet **Remove-AzEventHubGeoDRConfiguration** Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="356e7-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="356e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="356e7-110">EXAMPLES</span></span>

### <span data-ttu-id="356e7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="356e7-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="356e7-112">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="356e7-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="356e7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="356e7-113">PARAMETERS</span></span>

### <span data-ttu-id="356e7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="356e7-114">-AsJob</span></span>
<span data-ttu-id="356e7-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="356e7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="356e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e7-116">-DefaultProfile</span></span>
<span data-ttu-id="356e7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="356e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="356e7-118">-InputObject</span></span>
<span data-ttu-id="356e7-119">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="356e7-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="356e7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="356e7-120">-Name</span></span>
<span data-ttu-id="356e7-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="356e7-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="356e7-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="356e7-122">-Namespace</span></span>
<span data-ttu-id="356e7-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="356e7-123">Namespace Name</span></span>

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

### <span data-ttu-id="356e7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="356e7-124">-PassThru</span></span>
<span data-ttu-id="356e7-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="356e7-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="356e7-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="356e7-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="356e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="356e7-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="356e7-128">Resource Group Name</span></span>

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

### <span data-ttu-id="356e7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="356e7-129">-ResourceId</span></span>
<span data-ttu-id="356e7-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e7-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="356e7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="356e7-131">-Confirm</span></span>
<span data-ttu-id="356e7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="356e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356e7-133">-WhatIf</span></span>
<span data-ttu-id="356e7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="356e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356e7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="356e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e7-136">CommonParameters</span></span>
<span data-ttu-id="356e7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356e7-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356e7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="356e7-139">INPUTS</span></span>

### <span data-ttu-id="356e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="356e7-140">System.String</span></span>

### <span data-ttu-id="356e7-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="356e7-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="356e7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="356e7-142">OUTPUTS</span></span>

### <span data-ttu-id="356e7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="356e7-143">System.Boolean</span></span>

## <span data-ttu-id="356e7-144">Note</span><span class="sxs-lookup"><span data-stu-id="356e7-144">NOTES</span></span>

## <span data-ttu-id="356e7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="356e7-145">RELATED LINKS</span></span>
