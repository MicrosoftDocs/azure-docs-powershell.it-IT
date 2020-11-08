---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190290"
---
# <span data-ttu-id="34110-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="34110-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="34110-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34110-102">SYNOPSIS</span></span>
<span data-ttu-id="34110-103">Aggiorna il runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="34110-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="34110-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34110-104">SYNTAX</span></span>

### <span data-ttu-id="34110-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34110-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34110-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="34110-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34110-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="34110-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34110-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34110-108">DESCRIPTION</span></span>
<span data-ttu-id="34110-109">Il cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** aggiorna il runtime di integrazione ospitata autonomamente se la nuova versione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="34110-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="34110-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34110-110">EXAMPLES</span></span>

### <span data-ttu-id="34110-111">Esempio 1: aggiornare un runtime di integrazione ospitata autonomamente</span><span class="sxs-lookup"><span data-stu-id="34110-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="34110-112">Il cmdlet aggiorna il runtime di integrazione ospitale denominato "test-SelfHost-IR" in Factory di dati "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="34110-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="34110-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34110-113">PARAMETERS</span></span>

### <span data-ttu-id="34110-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="34110-114">-DataFactoryName</span></span>
<span data-ttu-id="34110-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="34110-115">The data factory name.</span></span>

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

### <span data-ttu-id="34110-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34110-116">-DefaultProfile</span></span>
<span data-ttu-id="34110-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34110-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34110-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34110-118">-InputObject</span></span>
<span data-ttu-id="34110-119">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="34110-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="34110-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="34110-120">-Name</span></span>
<span data-ttu-id="34110-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="34110-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34110-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34110-122">-ResourceGroupName</span></span>
<span data-ttu-id="34110-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34110-123">The resource group name.</span></span>

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

### <span data-ttu-id="34110-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34110-124">-ResourceId</span></span>
<span data-ttu-id="34110-125">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="34110-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="34110-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34110-126">-Confirm</span></span>
<span data-ttu-id="34110-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34110-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34110-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34110-128">-WhatIf</span></span>
<span data-ttu-id="34110-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34110-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34110-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34110-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34110-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34110-131">CommonParameters</span></span>
<span data-ttu-id="34110-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34110-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34110-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34110-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34110-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34110-134">INPUTS</span></span>

### <span data-ttu-id="34110-135">System. String</span><span class="sxs-lookup"><span data-stu-id="34110-135">System.String</span></span>

### <span data-ttu-id="34110-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="34110-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="34110-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34110-137">OUTPUTS</span></span>

### <span data-ttu-id="34110-138">System. void</span><span class="sxs-lookup"><span data-stu-id="34110-138">System.Void</span></span>

## <span data-ttu-id="34110-139">Note</span><span class="sxs-lookup"><span data-stu-id="34110-139">NOTES</span></span>
<span data-ttu-id="34110-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="34110-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="34110-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34110-141">RELATED LINKS</span></span>

<span data-ttu-id="34110-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="34110-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

