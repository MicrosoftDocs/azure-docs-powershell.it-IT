---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186231"
---
# <span data-ttu-id="285c7-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="285c7-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="285c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285c7-102">SYNOPSIS</span></span>
<span data-ttu-id="285c7-103">Avvia un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="285c7-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="285c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="285c7-104">SYNTAX</span></span>

### <span data-ttu-id="285c7-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="285c7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="285c7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="285c7-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285c7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="285c7-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285c7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="285c7-108">DESCRIPTION</span></span>
<span data-ttu-id="285c7-109">Il cmdlet **Start-AzDataFactoryV2IntegrationRuntime avvia** un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="285c7-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="285c7-110">Viene effettuato il provisioning della risorsa e, dopo l'operazione, lo stato è "Avviato".</span><span class="sxs-lookup"><span data-stu-id="285c7-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="285c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="285c7-111">EXAMPLES</span></span>

### <span data-ttu-id="285c7-112">Esempio 1: Avviare un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="285c7-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="285c7-113">Questo cmdlet avvia un runtime di integrazione dedicato gestito denominato "test-dedicated-ir".</span><span class="sxs-lookup"><span data-stu-id="285c7-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="285c7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285c7-114">PARAMETERS</span></span>

### <span data-ttu-id="285c7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="285c7-115">-DataFactoryName</span></span>
<span data-ttu-id="285c7-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="285c7-116">The data factory name.</span></span>

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

### <span data-ttu-id="285c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285c7-117">-DefaultProfile</span></span>
<span data-ttu-id="285c7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="285c7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285c7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="285c7-119">-Force</span></span>
<span data-ttu-id="285c7-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="285c7-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="285c7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="285c7-121">-InputObject</span></span>
<span data-ttu-id="285c7-122">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="285c7-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="285c7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="285c7-123">-Name</span></span>
<span data-ttu-id="285c7-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="285c7-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="285c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="285c7-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="285c7-126">The resource group name.</span></span>

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

### <span data-ttu-id="285c7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="285c7-127">-ResourceId</span></span>
<span data-ttu-id="285c7-128">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="285c7-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="285c7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285c7-129">-Confirm</span></span>
<span data-ttu-id="285c7-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="285c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="285c7-131">-WhatIf</span></span>
<span data-ttu-id="285c7-132">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="285c7-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="285c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285c7-133">CommonParameters</span></span>
<span data-ttu-id="285c7-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285c7-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285c7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285c7-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="285c7-136">INPUTS</span></span>

### <span data-ttu-id="285c7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="285c7-137">System.String</span></span>

### <span data-ttu-id="285c7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="285c7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="285c7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="285c7-139">OUTPUTS</span></span>

### <span data-ttu-id="285c7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="285c7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="285c7-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="285c7-141">NOTES</span></span>

## <span data-ttu-id="285c7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="285c7-142">RELATED LINKS</span></span>

[<span data-ttu-id="285c7-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="285c7-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
