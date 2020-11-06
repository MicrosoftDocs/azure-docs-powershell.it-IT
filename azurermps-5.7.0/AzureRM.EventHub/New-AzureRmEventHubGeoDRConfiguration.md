---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: feeb47a1db28debfcfeb4e5d61c22e15db66b799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511179"
---
# <span data-ttu-id="ed8e2-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed8e2-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="ed8e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8e2-103">Crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="ed8e2-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed8e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed8e2-104">SYNTAX</span></span>

### <span data-ttu-id="ed8e2-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed8e2-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8e2-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed8e2-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8e2-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed8e2-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed8e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed8e2-108">DESCRIPTION</span></span>
<span data-ttu-id="ed8e2-109">Il cmdlet **New-AzureRmEventHubGeoDRConfiguration** crea un nuovo alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="ed8e2-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="ed8e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed8e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ed8e2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed8e2-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="ed8e2-112">Crea un alias "SampleDRCongifName" con lo spazio dei nomi principale "SampleNamespace_Primary" con lo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="ed8e2-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="ed8e2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed8e2-113">PARAMETERS</span></span>

### <span data-ttu-id="ed8e2-114">-Alternaname</span><span class="sxs-lookup"><span data-stu-id="ed8e2-114">-AlternateName</span></span>
<span data-ttu-id="ed8e2-115">Alternate obbligatorio quando il nome della configurazione DR è lo stesso dello spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="ed8e2-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed8e2-116">-AsJob</span></span>
<span data-ttu-id="ed8e2-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed8e2-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8e2-118">-DefaultProfile</span></span>
<span data-ttu-id="ed8e2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8e2-120">-InputObject</span></span>
<span data-ttu-id="ed8e2-121">Oggetto Namespace</span><span class="sxs-lookup"><span data-stu-id="ed8e2-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed8e2-122">-Name</span></span>
<span data-ttu-id="ed8e2-123">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="ed8e2-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed8e2-124">-Namespace</span></span>
<span data-ttu-id="ed8e2-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed8e2-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="ed8e2-126">-PartnerNamespace</span></span>
<span data-ttu-id="ed8e2-127">PartnerNamespace configurazione DR</span><span class="sxs-lookup"><span data-stu-id="ed8e2-127">DR Configuration PartnerNamespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed8e2-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ed8e2-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8e2-130">-ResourceId</span></span>
<span data-ttu-id="ed8e2-131">ID risorsa dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed8e2-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed8e2-132">-Confirm</span></span>
<span data-ttu-id="ed8e2-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8e2-134">-WhatIf</span></span>
<span data-ttu-id="ed8e2-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8e2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8e2-137">CommonParameters</span></span>
<span data-ttu-id="ed8e2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed8e2-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8e2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8e2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed8e2-140">INPUTS</span></span>

### <span data-ttu-id="ed8e2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8e2-141">System.String</span></span>
<span data-ttu-id="ed8e2-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ed8e2-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="ed8e2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed8e2-143">OUTPUTS</span></span>

### <span data-ttu-id="ed8e2-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ed8e2-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="ed8e2-145">Note</span><span class="sxs-lookup"><span data-stu-id="ed8e2-145">NOTES</span></span>

## <span data-ttu-id="ed8e2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed8e2-146">RELATED LINKS</span></span>
