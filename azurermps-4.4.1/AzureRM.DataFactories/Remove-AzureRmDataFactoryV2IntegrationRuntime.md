---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518303"
---
# <span data-ttu-id="9ae81-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ae81-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="9ae81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ae81-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae81-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9ae81-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ae81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae81-104">SYNTAX</span></span>

### <span data-ttu-id="9ae81-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ae81-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ae81-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae81-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae81-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9ae81-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ae81-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae81-109">Il cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9ae81-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="9ae81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae81-110">EXAMPLES</span></span>

### <span data-ttu-id="9ae81-111">Esempio 1: rimuovere un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="9ae81-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="9ae81-112">Questo comando rimuove l'Integration runtime denominato ' test-reserved-IR ' dalla data factory denominata ' test-DF '.</span><span class="sxs-lookup"><span data-stu-id="9ae81-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="9ae81-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="9ae81-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="9ae81-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ae81-114">PARAMETERS</span></span>

### <span data-ttu-id="9ae81-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9ae81-115">-DataFactoryName</span></span>
<span data-ttu-id="9ae81-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="9ae81-116">The data factory name.</span></span>

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

### <span data-ttu-id="9ae81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9ae81-117">-Force</span></span>
<span data-ttu-id="9ae81-118">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9ae81-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9ae81-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ae81-119">-InputObject</span></span>
<span data-ttu-id="9ae81-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="9ae81-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="9ae81-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ae81-121">-Name</span></span>
<span data-ttu-id="9ae81-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9ae81-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="9ae81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae81-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ae81-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ae81-124">The resource group name.</span></span>

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

### <span data-ttu-id="9ae81-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae81-125">-ResourceId</span></span>
<span data-ttu-id="9ae81-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae81-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9ae81-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ae81-127">-Confirm</span></span>
<span data-ttu-id="9ae81-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae81-129">-WhatIf</span></span>
<span data-ttu-id="9ae81-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ae81-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9ae81-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae81-131">-DefaultProfile</span></span>
<span data-ttu-id="9ae81-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae81-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae81-133">CommonParameters</span></span>
<span data-ttu-id="9ae81-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae81-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae81-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae81-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ae81-136">INPUTS</span></span>

### <span data-ttu-id="9ae81-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9ae81-137">System.String</span></span>
<span data-ttu-id="9ae81-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ae81-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9ae81-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae81-139">OUTPUTS</span></span>

### <span data-ttu-id="9ae81-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="9ae81-140">System.Object</span></span>

## <span data-ttu-id="9ae81-141">Note</span><span class="sxs-lookup"><span data-stu-id="9ae81-141">NOTES</span></span>
<span data-ttu-id="9ae81-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="9ae81-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="9ae81-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae81-143">RELATED LINKS</span></span>

[<span data-ttu-id="9ae81-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ae81-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="9ae81-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9ae81-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

