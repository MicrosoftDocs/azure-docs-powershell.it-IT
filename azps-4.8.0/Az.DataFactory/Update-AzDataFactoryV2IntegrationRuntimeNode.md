---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190277"
---
# <span data-ttu-id="ab632-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ab632-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ab632-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab632-102">SYNOPSIS</span></span>
<span data-ttu-id="ab632-103">Aggiorna il nodo runtime di Integration self-hosted.</span><span class="sxs-lookup"><span data-stu-id="ab632-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="ab632-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab632-104">SYNTAX</span></span>

### <span data-ttu-id="ab632-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab632-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab632-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab632-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab632-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ab632-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab632-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab632-108">DESCRIPTION</span></span>
<span data-ttu-id="ab632-109">Il cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** aggiorna le proprietà del nodo runtime di integrazione ospitata in una data factory.</span><span class="sxs-lookup"><span data-stu-id="ab632-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="ab632-110">Attualmente supporta solo l'aggiornamento di "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="ab632-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="ab632-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab632-111">EXAMPLES</span></span>

### <span data-ttu-id="ab632-112">Esempio 1: aggiorna il nodo runtime di integrazione ospitata autonomamente</span><span class="sxs-lookup"><span data-stu-id="ab632-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="ab632-113">Il cmdlet aggiorna "ConcurrentJobsLimit" in 3 per il nodo "Node_1" in self-hosted Integration Runtime "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="ab632-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ab632-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab632-114">PARAMETERS</span></span>

### <span data-ttu-id="ab632-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="ab632-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="ab632-116">Numero di processi simultanei consentiti per l'esecuzione nel nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="ab632-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="ab632-117">I valori compresi tra 1 e maxConcurrentJobs sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="ab632-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab632-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ab632-118">-DataFactoryName</span></span>
<span data-ttu-id="ab632-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="ab632-119">The data factory name.</span></span>

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

### <span data-ttu-id="ab632-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab632-120">-DefaultProfile</span></span>
<span data-ttu-id="ab632-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab632-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab632-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab632-122">-InputObject</span></span>
<span data-ttu-id="ab632-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="ab632-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ab632-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ab632-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ab632-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ab632-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ab632-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab632-126">-Name</span></span>
<span data-ttu-id="ab632-127">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="ab632-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab632-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab632-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab632-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab632-129">The resource group name.</span></span>

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

### <span data-ttu-id="ab632-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab632-130">-ResourceId</span></span>
<span data-ttu-id="ab632-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab632-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ab632-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab632-132">-Confirm</span></span>
<span data-ttu-id="ab632-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab632-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab632-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab632-134">-WhatIf</span></span>
<span data-ttu-id="ab632-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab632-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab632-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab632-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab632-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab632-137">CommonParameters</span></span>
<span data-ttu-id="ab632-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab632-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab632-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab632-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab632-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab632-140">INPUTS</span></span>

### <span data-ttu-id="ab632-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ab632-141">System.String</span></span>

### <span data-ttu-id="ab632-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ab632-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ab632-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab632-143">OUTPUTS</span></span>

### <span data-ttu-id="ab632-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ab632-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ab632-145">Note</span><span class="sxs-lookup"><span data-stu-id="ab632-145">NOTES</span></span>
<span data-ttu-id="ab632-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ab632-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ab632-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab632-147">RELATED LINKS</span></span>

<span data-ttu-id="ab632-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="ab632-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

