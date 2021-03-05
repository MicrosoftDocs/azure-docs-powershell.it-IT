---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 941e820bb1c274a74cc52042b80cdf1b259a34b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975101"
---
# <span data-ttu-id="b2cd1-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="b2cd1-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="b2cd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cd1-103">Aggiorna il runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="b2cd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2cd1-104">SYNTAX</span></span>

### <span data-ttu-id="b2cd1-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2cd1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2cd1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2cd1-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2cd1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b2cd1-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2cd1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2cd1-108">DESCRIPTION</span></span>
<span data-ttu-id="b2cd1-109">Il cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** aggiorna il runtime di integrazione self-hosted, se la nuova versione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="b2cd1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2cd1-110">EXAMPLES</span></span>

### <span data-ttu-id="b2cd1-111">Esempio 1: Aggiorna un runtime di integrazione self-hosted</span><span class="sxs-lookup"><span data-stu-id="b2cd1-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="b2cd1-112">Il cmdlet aggiorna il runtime di integrazione self-hosted denominato "test-selfhost-ir" nel data factory 'test-df-eu2'.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="b2cd1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2cd1-113">PARAMETERS</span></span>

### <span data-ttu-id="b2cd1-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2cd1-114">-DataFactoryName</span></span>
<span data-ttu-id="b2cd1-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-115">The data factory name.</span></span>

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

### <span data-ttu-id="b2cd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cd1-116">-DefaultProfile</span></span>
<span data-ttu-id="b2cd1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cd1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2cd1-118">-InputObject</span></span>
<span data-ttu-id="b2cd1-119">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="b2cd1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b2cd1-120">-Name</span></span>
<span data-ttu-id="b2cd1-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="b2cd1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2cd1-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2cd1-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-123">The resource group name.</span></span>

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

### <span data-ttu-id="b2cd1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2cd1-124">-ResourceId</span></span>
<span data-ttu-id="b2cd1-125">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b2cd1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2cd1-126">-Confirm</span></span>
<span data-ttu-id="b2cd1-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2cd1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2cd1-128">-WhatIf</span></span>
<span data-ttu-id="b2cd1-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2cd1-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2cd1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cd1-131">CommonParameters</span></span>
<span data-ttu-id="b2cd1-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cd1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cd1-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cd1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cd1-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2cd1-134">INPUTS</span></span>

### <span data-ttu-id="b2cd1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b2cd1-135">System.String</span></span>

### <span data-ttu-id="b2cd1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b2cd1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b2cd1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2cd1-137">OUTPUTS</span></span>

### <span data-ttu-id="b2cd1-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="b2cd1-138">System.Void</span></span>

## <span data-ttu-id="b2cd1-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2cd1-139">NOTES</span></span>
<span data-ttu-id="b2cd1-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="b2cd1-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b2cd1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2cd1-141">RELATED LINKS</span></span>

<span data-ttu-id="b2cd1-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="b2cd1-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

