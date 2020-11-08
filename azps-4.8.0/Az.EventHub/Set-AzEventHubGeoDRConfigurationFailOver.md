---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031745"
---
# <span data-ttu-id="4a86a-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="4a86a-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="4a86a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a86a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a86a-103">Richiama il failover GEO DR e riconfigura l'alias per puntare allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="4a86a-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="4a86a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a86a-104">SYNTAX</span></span>

### <span data-ttu-id="4a86a-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a86a-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a86a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a86a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a86a-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a86a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a86a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a86a-108">DESCRIPTION</span></span>
<span data-ttu-id="4a86a-109">Il cmdlet **set-AzEventHubGeoDRConfigurationFailOver** richiama il failover Geo Dr e riconfigura l'alias per puntare allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="4a86a-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="4a86a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a86a-110">EXAMPLES</span></span>

### <span data-ttu-id="4a86a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a86a-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="4a86a-112">Richiama il failover su alias "SampleDRConfigName", riconfigura e punta allo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="4a86a-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="4a86a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a86a-113">PARAMETERS</span></span>

### <span data-ttu-id="4a86a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a86a-114">-DefaultProfile</span></span>
<span data-ttu-id="4a86a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a86a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a86a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a86a-116">-InputObject</span></span>
<span data-ttu-id="4a86a-117">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="4a86a-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="4a86a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a86a-118">-Name</span></span>
<span data-ttu-id="4a86a-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="4a86a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="4a86a-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a86a-120">-Namespace</span></span>
<span data-ttu-id="4a86a-121">Nome dello spazio dei nomi-spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="4a86a-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="4a86a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a86a-122">-PassThru</span></span>
<span data-ttu-id="4a86a-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4a86a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a86a-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4a86a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a86a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a86a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a86a-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4a86a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4a86a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a86a-127">-ResourceId</span></span>
<span data-ttu-id="4a86a-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a86a-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="4a86a-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a86a-129">-Confirm</span></span>
<span data-ttu-id="4a86a-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a86a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a86a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a86a-131">-WhatIf</span></span>
<span data-ttu-id="4a86a-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a86a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a86a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a86a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a86a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a86a-134">CommonParameters</span></span>
<span data-ttu-id="4a86a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a86a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a86a-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a86a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a86a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a86a-137">INPUTS</span></span>

### <span data-ttu-id="4a86a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a86a-138">System.String</span></span>

### <span data-ttu-id="4a86a-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4a86a-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="4a86a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a86a-140">OUTPUTS</span></span>

### <span data-ttu-id="4a86a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a86a-141">System.Boolean</span></span>

## <span data-ttu-id="4a86a-142">Note</span><span class="sxs-lookup"><span data-stu-id="4a86a-142">NOTES</span></span>

## <span data-ttu-id="4a86a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a86a-143">RELATED LINKS</span></span>
