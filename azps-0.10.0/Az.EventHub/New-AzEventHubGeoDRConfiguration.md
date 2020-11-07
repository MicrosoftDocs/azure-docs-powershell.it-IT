---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2c48ad3bda14775dd0535b63343d90f026bf614
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861470"
---
# <span data-ttu-id="07df3-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="07df3-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="07df3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07df3-102">SYNOPSIS</span></span>
<span data-ttu-id="07df3-103">Crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="07df3-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="07df3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07df3-104">SYNTAX</span></span>

### <span data-ttu-id="07df3-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07df3-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07df3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="07df3-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07df3-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07df3-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07df3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07df3-108">DESCRIPTION</span></span>
<span data-ttu-id="07df3-109">Il cmdlet **New-AzEventHubGeoDRConfiguration** crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="07df3-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="07df3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07df3-110">EXAMPLES</span></span>

### <span data-ttu-id="07df3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07df3-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="07df3-112">Crea un alias "SampleDRConfigName" con lo spazio dei nomi principale "SampleNamespace_Primary" con lo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="07df3-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="07df3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07df3-113">PARAMETERS</span></span>

### <span data-ttu-id="07df3-114">-Alternaname</span><span class="sxs-lookup"><span data-stu-id="07df3-114">-AlternateName</span></span>
<span data-ttu-id="07df3-115">Alternate obbligatorio quando il nome della configurazione DR è lo stesso dello spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="07df3-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="07df3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07df3-116">-AsJob</span></span>
<span data-ttu-id="07df3-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07df3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07df3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07df3-118">-DefaultProfile</span></span>
<span data-ttu-id="07df3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07df3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07df3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07df3-120">-InputObject</span></span>
<span data-ttu-id="07df3-121">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="07df3-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07df3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="07df3-122">-Name</span></span>
<span data-ttu-id="07df3-123">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="07df3-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07df3-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07df3-124">-Namespace</span></span>
<span data-ttu-id="07df3-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07df3-125">Namespace Name</span></span>

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

### <span data-ttu-id="07df3-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="07df3-126">-PartnerNamespace</span></span>
<span data-ttu-id="07df3-127">PartnerNamespace configurazione DR</span><span class="sxs-lookup"><span data-stu-id="07df3-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07df3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07df3-128">-ResourceGroupName</span></span>
<span data-ttu-id="07df3-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="07df3-129">Resource Group Name</span></span>

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

### <span data-ttu-id="07df3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07df3-130">-ResourceId</span></span>
<span data-ttu-id="07df3-131">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07df3-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07df3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07df3-132">-Confirm</span></span>
<span data-ttu-id="07df3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07df3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07df3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07df3-134">-WhatIf</span></span>
<span data-ttu-id="07df3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07df3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07df3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07df3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07df3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07df3-137">CommonParameters</span></span>
<span data-ttu-id="07df3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07df3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07df3-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07df3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07df3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07df3-140">INPUTS</span></span>

### <span data-ttu-id="07df3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="07df3-141">System.String</span></span>

### <span data-ttu-id="07df3-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="07df3-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="07df3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07df3-143">OUTPUTS</span></span>

### <span data-ttu-id="07df3-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="07df3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="07df3-145">Note</span><span class="sxs-lookup"><span data-stu-id="07df3-145">NOTES</span></span>

## <span data-ttu-id="07df3-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07df3-146">RELATED LINKS</span></span>
