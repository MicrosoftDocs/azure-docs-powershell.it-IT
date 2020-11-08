---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203592"
---
# <span data-ttu-id="86287-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86287-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="86287-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86287-102">SYNOPSIS</span></span>
<span data-ttu-id="86287-103">Rimuove la configurazione batch di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="86287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86287-104">SYNTAX</span></span>

### <span data-ttu-id="86287-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86287-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86287-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86287-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86287-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86287-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86287-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86287-108">DESCRIPTION</span></span>
<span data-ttu-id="86287-109">Il cmdlet **Remove-AzIntegrationAccountBatchConfiguration** rimuove una configurazione batch da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="86287-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86287-110">EXAMPLES</span></span>

### <span data-ttu-id="86287-111">Esempio 1: rimuovere una configurazione batch per parametri</span><span class="sxs-lookup"><span data-stu-id="86287-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="86287-112">Rimuove la configurazione batch denominata "sampleBatchConfig" situata nell'account di integrazione "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="86287-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="86287-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86287-113">PARAMETERS</span></span>

### <span data-ttu-id="86287-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86287-114">-DefaultProfile</span></span>
<span data-ttu-id="86287-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86287-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86287-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86287-116">-InputObject</span></span>
<span data-ttu-id="86287-117">Configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86287-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="86287-118">-Name</span></span>
<span data-ttu-id="86287-119">Nome della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86287-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="86287-120">-ParentName</span></span>
<span data-ttu-id="86287-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86287-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86287-122">-PassThru</span></span>
<span data-ttu-id="86287-123">Restituirà se il comando ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="86287-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="86287-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86287-124">-ResourceGroupName</span></span>
<span data-ttu-id="86287-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86287-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86287-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86287-126">-ResourceId</span></span>
<span data-ttu-id="86287-127">ID risorsa configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86287-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86287-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86287-128">-Confirm</span></span>
<span data-ttu-id="86287-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86287-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86287-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86287-130">-WhatIf</span></span>
<span data-ttu-id="86287-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86287-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86287-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86287-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86287-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86287-133">CommonParameters</span></span>
<span data-ttu-id="86287-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86287-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86287-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86287-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86287-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86287-136">INPUTS</span></span>

### <span data-ttu-id="86287-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="86287-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="86287-138">System. String</span><span class="sxs-lookup"><span data-stu-id="86287-138">System.String</span></span>

## <span data-ttu-id="86287-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86287-139">OUTPUTS</span></span>

### <span data-ttu-id="86287-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86287-140">System.Boolean</span></span>

## <span data-ttu-id="86287-141">Note</span><span class="sxs-lookup"><span data-stu-id="86287-141">NOTES</span></span>

## <span data-ttu-id="86287-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86287-142">RELATED LINKS</span></span>
