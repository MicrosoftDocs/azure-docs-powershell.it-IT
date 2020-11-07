---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836427"
---
# <span data-ttu-id="4a0cc-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="4a0cc-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="4a0cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a0cc-103">Sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="4a0cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a0cc-104">SYNTAX</span></span>

### <span data-ttu-id="4a0cc-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a0cc-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0cc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a0cc-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a0cc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4a0cc-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a0cc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a0cc-108">DESCRIPTION</span></span>
<span data-ttu-id="4a0cc-109">Il cmdlet **Sync-AzDataFactoryV2IntegrationRuntimeCredential** sincronizza le credenziali locali tra i nodi di Integration Runtime, che obbligano le credenziali a essere identiche in tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="4a0cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a0cc-110">EXAMPLES</span></span>

### <span data-ttu-id="4a0cc-111">Esempio 1: sincronizzare una credenziale di Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4a0cc-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="4a0cc-112">Il cmdlet sincronizza le credenziali tra i nodi di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="4a0cc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a0cc-113">PARAMETERS</span></span>

### <span data-ttu-id="4a0cc-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4a0cc-114">-DataFactoryName</span></span>
<span data-ttu-id="4a0cc-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a0cc-116">-DefaultProfile</span></span>
<span data-ttu-id="4a0cc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a0cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4a0cc-118">-Force</span></span>
<span data-ttu-id="4a0cc-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4a0cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a0cc-120">-InputObject</span></span>
<span data-ttu-id="4a0cc-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0cc-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4a0cc-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4a0cc-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a0cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a0cc-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a0cc-126">-ResourceId</span></span>
<span data-ttu-id="4a0cc-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a0cc-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a0cc-128">-Confirm</span></span>
<span data-ttu-id="4a0cc-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a0cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a0cc-130">-WhatIf</span></span>
<span data-ttu-id="4a0cc-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4a0cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a0cc-132">CommonParameters</span></span>
<span data-ttu-id="4a0cc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a0cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a0cc-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a0cc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a0cc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a0cc-135">INPUTS</span></span>

### <span data-ttu-id="4a0cc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4a0cc-136">System.String</span></span>

### <span data-ttu-id="4a0cc-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4a0cc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4a0cc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a0cc-138">OUTPUTS</span></span>

### <span data-ttu-id="4a0cc-139">System. void</span><span class="sxs-lookup"><span data-stu-id="4a0cc-139">System.Void</span></span>

## <span data-ttu-id="4a0cc-140">Note</span><span class="sxs-lookup"><span data-stu-id="4a0cc-140">NOTES</span></span>

## <span data-ttu-id="4a0cc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a0cc-141">RELATED LINKS</span></span>
