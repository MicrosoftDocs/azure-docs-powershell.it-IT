---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190795"
---
# <span data-ttu-id="8eeab-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8eeab-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="8eeab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8eeab-102">SYNOPSIS</span></span>
<span data-ttu-id="8eeab-103">Avvia un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="8eeab-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="8eeab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eeab-104">SYNTAX</span></span>

### <span data-ttu-id="8eeab-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8eeab-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eeab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8eeab-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eeab-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8eeab-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eeab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8eeab-108">DESCRIPTION</span></span>
<span data-ttu-id="8eeab-109">Il cmdlet **Start-AzDataFactoryV2IntegrationRuntime** avvia un runtime di Integration dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="8eeab-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="8eeab-110">La risorsa viene provisionata e dopo l'operazione lo stato è "iniziato".</span><span class="sxs-lookup"><span data-stu-id="8eeab-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="8eeab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eeab-111">EXAMPLES</span></span>

### <span data-ttu-id="8eeab-112">Esempio 1: avviare un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="8eeab-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="8eeab-113">Questo cmdlet avvia un runtime di integrazione dedicata gestito denominato test-Dedicated-IR.</span><span class="sxs-lookup"><span data-stu-id="8eeab-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="8eeab-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8eeab-114">PARAMETERS</span></span>

### <span data-ttu-id="8eeab-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8eeab-115">-DataFactoryName</span></span>
<span data-ttu-id="8eeab-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8eeab-116">The data factory name.</span></span>

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

### <span data-ttu-id="8eeab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eeab-117">-DefaultProfile</span></span>
<span data-ttu-id="8eeab-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8eeab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eeab-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8eeab-119">-Force</span></span>
<span data-ttu-id="8eeab-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8eeab-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8eeab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eeab-121">-InputObject</span></span>
<span data-ttu-id="8eeab-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="8eeab-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="8eeab-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eeab-123">-Name</span></span>
<span data-ttu-id="8eeab-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8eeab-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="8eeab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eeab-125">-ResourceGroupName</span></span>
<span data-ttu-id="8eeab-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8eeab-126">The resource group name.</span></span>

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

### <span data-ttu-id="8eeab-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eeab-127">-ResourceId</span></span>
<span data-ttu-id="8eeab-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8eeab-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8eeab-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8eeab-129">-Confirm</span></span>
<span data-ttu-id="8eeab-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8eeab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eeab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eeab-131">-WhatIf</span></span>
<span data-ttu-id="8eeab-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8eeab-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8eeab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eeab-133">CommonParameters</span></span>
<span data-ttu-id="8eeab-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eeab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eeab-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eeab-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eeab-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8eeab-136">INPUTS</span></span>

### <span data-ttu-id="8eeab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8eeab-137">System.String</span></span>

### <span data-ttu-id="8eeab-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8eeab-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8eeab-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eeab-139">OUTPUTS</span></span>

### <span data-ttu-id="8eeab-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="8eeab-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="8eeab-141">Note</span><span class="sxs-lookup"><span data-stu-id="8eeab-141">NOTES</span></span>

## <span data-ttu-id="8eeab-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eeab-142">RELATED LINKS</span></span>

[<span data-ttu-id="8eeab-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8eeab-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
