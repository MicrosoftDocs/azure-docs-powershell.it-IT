---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 20fe97e27a4129a727cad7c8dc38935887e3968e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674407"
---
# <span data-ttu-id="b634d-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="b634d-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="b634d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b634d-102">SYNOPSIS</span></span>
<span data-ttu-id="b634d-103">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="b634d-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="b634d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b634d-104">SYNTAX</span></span>

### <span data-ttu-id="b634d-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b634d-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b634d-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b634d-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b634d-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b634d-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b634d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b634d-108">DESCRIPTION</span></span>
<span data-ttu-id="b634d-109">Il cmdlet **set-AzEventHubGeoDRConfigurationBreakPair** Disabilita il ripristino di emergenza e smette di replicare le modifiche dagli spazi dei nomi secondari principali a</span><span class="sxs-lookup"><span data-stu-id="b634d-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="b634d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b634d-110">EXAMPLES</span></span>

### <span data-ttu-id="b634d-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="b634d-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="b634d-112">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="b634d-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="b634d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b634d-113">PARAMETERS</span></span>

### <span data-ttu-id="b634d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b634d-114">-DefaultProfile</span></span>
<span data-ttu-id="b634d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b634d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b634d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b634d-116">-InputObject</span></span>
<span data-ttu-id="b634d-117">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="b634d-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="b634d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b634d-118">-Name</span></span>
<span data-ttu-id="b634d-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="b634d-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="b634d-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b634d-120">-Namespace</span></span>
<span data-ttu-id="b634d-121">Nome dello spazio dei nomi-spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="b634d-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="b634d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b634d-122">-PassThru</span></span>
<span data-ttu-id="b634d-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b634d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b634d-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b634d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b634d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b634d-125">-ResourceGroupName</span></span>
<span data-ttu-id="b634d-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b634d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b634d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b634d-127">-ResourceId</span></span>
<span data-ttu-id="b634d-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b634d-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b634d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b634d-129">-Confirm</span></span>
<span data-ttu-id="b634d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b634d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b634d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b634d-131">-WhatIf</span></span>
<span data-ttu-id="b634d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b634d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b634d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b634d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b634d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b634d-134">CommonParameters</span></span>
<span data-ttu-id="b634d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b634d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b634d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b634d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b634d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b634d-137">INPUTS</span></span>

### <span data-ttu-id="b634d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b634d-138">System.String</span></span>

### <span data-ttu-id="b634d-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b634d-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="b634d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b634d-140">OUTPUTS</span></span>

### <span data-ttu-id="b634d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b634d-141">System.Boolean</span></span>

## <span data-ttu-id="b634d-142">Note</span><span class="sxs-lookup"><span data-stu-id="b634d-142">NOTES</span></span>

## <span data-ttu-id="b634d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b634d-143">RELATED LINKS</span></span>
