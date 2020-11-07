---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685687"
---
# <span data-ttu-id="744e6-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="744e6-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="744e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="744e6-102">SYNOPSIS</span></span>
<span data-ttu-id="744e6-103">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="744e6-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="744e6-104">SYNTAX</span></span>

### <span data-ttu-id="744e6-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="744e6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="744e6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="744e6-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="744e6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="744e6-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="744e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="744e6-108">DESCRIPTION</span></span>
<span data-ttu-id="744e6-109">Il cmdlet **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di Integration Runtime, che obbligano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="744e6-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="744e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="744e6-110">EXAMPLES</span></span>

### <span data-ttu-id="744e6-111">Esempio 1: sincronizzare una credenziale di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="744e6-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="744e6-112">Il cmdlet sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="744e6-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="744e6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="744e6-113">PARAMETERS</span></span>

### <span data-ttu-id="744e6-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="744e6-114">-Confirm</span></span>
<span data-ttu-id="744e6-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="744e6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744e6-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="744e6-116">-DataFactoryName</span></span>
<span data-ttu-id="744e6-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="744e6-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="744e6-118">-Force</span></span>
<span data-ttu-id="744e6-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="744e6-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="744e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="744e6-120">-InputObject</span></span>
<span data-ttu-id="744e6-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="744e6-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="744e6-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="744e6-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="744e6-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="744e6-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="744e6-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="744e6-126">-ResourceId</span></span>
<span data-ttu-id="744e6-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="744e6-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744e6-128">-WhatIf</span></span>
<span data-ttu-id="744e6-129">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="744e6-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="744e6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="744e6-130">INPUTS</span></span>

### <span data-ttu-id="744e6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="744e6-131">System.String</span></span>
<span data-ttu-id="744e6-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="744e6-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="744e6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="744e6-133">OUTPUTS</span></span>

### <span data-ttu-id="744e6-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="744e6-134">System.Object</span></span>

## <span data-ttu-id="744e6-135">Note</span><span class="sxs-lookup"><span data-stu-id="744e6-135">NOTES</span></span>

## <span data-ttu-id="744e6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="744e6-136">RELATED LINKS</span></span>
