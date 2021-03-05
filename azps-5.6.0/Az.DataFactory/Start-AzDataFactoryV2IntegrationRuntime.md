---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: eeb0db5c9dd180d8194d0bd506296f269c6c5386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964894"
---
# <span data-ttu-id="e2940-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2940-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e2940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2940-102">SYNOPSIS</span></span>
<span data-ttu-id="e2940-103">Avvia un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="e2940-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="e2940-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2940-104">SYNTAX</span></span>

### <span data-ttu-id="e2940-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2940-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2940-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2940-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2940-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e2940-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2940-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e2940-108">DESCRIPTION</span></span>
<span data-ttu-id="e2940-109">Il cmdlet **Start-AzDataFactoryV2IntegrationRuntime avvia** un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="e2940-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="e2940-110">Viene effettuato il provisioning della risorsa e, dopo l'operazione, lo stato è "Avviato".</span><span class="sxs-lookup"><span data-stu-id="e2940-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="e2940-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2940-111">EXAMPLES</span></span>

### <span data-ttu-id="e2940-112">Esempio 1: Avviare un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="e2940-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="e2940-113">Questo cmdlet avvia un runtime di integrazione dedicato gestito denominato "test-dedicated-ir".</span><span class="sxs-lookup"><span data-stu-id="e2940-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="e2940-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2940-114">PARAMETERS</span></span>

### <span data-ttu-id="e2940-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e2940-115">-DataFactoryName</span></span>
<span data-ttu-id="e2940-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="e2940-116">The data factory name.</span></span>

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

### <span data-ttu-id="e2940-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2940-117">-DefaultProfile</span></span>
<span data-ttu-id="e2940-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2940-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2940-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e2940-119">-Force</span></span>
<span data-ttu-id="e2940-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e2940-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e2940-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2940-121">-InputObject</span></span>
<span data-ttu-id="e2940-122">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e2940-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e2940-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e2940-123">-Name</span></span>
<span data-ttu-id="e2940-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e2940-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="e2940-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2940-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2940-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2940-126">The resource group name.</span></span>

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

### <span data-ttu-id="e2940-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2940-127">-ResourceId</span></span>
<span data-ttu-id="e2940-128">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="e2940-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e2940-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2940-129">-Confirm</span></span>
<span data-ttu-id="e2940-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2940-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2940-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2940-131">-WhatIf</span></span>
<span data-ttu-id="e2940-132">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="e2940-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e2940-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2940-133">CommonParameters</span></span>
<span data-ttu-id="e2940-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2940-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2940-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2940-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2940-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e2940-136">INPUTS</span></span>

### <span data-ttu-id="e2940-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e2940-137">System.String</span></span>

### <span data-ttu-id="e2940-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2940-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e2940-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2940-139">OUTPUTS</span></span>

### <span data-ttu-id="e2940-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e2940-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e2940-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e2940-141">NOTES</span></span>

## <span data-ttu-id="e2940-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2940-142">RELATED LINKS</span></span>

[<span data-ttu-id="e2940-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2940-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
