---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 24c5f3b93b2be446eed4e5b81e1e69bf2116aa8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961966"
---
# <span data-ttu-id="ed95e-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed95e-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="ed95e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed95e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed95e-103">Rimuove una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="ed95e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed95e-104">SYNTAX</span></span>

### <span data-ttu-id="ed95e-105">ByIntegrationAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed95e-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed95e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed95e-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed95e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed95e-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed95e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed95e-108">DESCRIPTION</span></span>
<span data-ttu-id="ed95e-109">Il cmdlet **Remove-AzIntegrationAccountBatchConfiguration** rimuove una configurazione batch da un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="ed95e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed95e-110">EXAMPLES</span></span>

### <span data-ttu-id="ed95e-111">Esempio 1: Rimuovere una configurazione batch in base ai parametri</span><span class="sxs-lookup"><span data-stu-id="ed95e-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="ed95e-112">Rimuove la configurazione batch denominata "sampleBatchConfig" che si trova nell'account di integrazione "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="ed95e-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="ed95e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed95e-113">PARAMETERS</span></span>

### <span data-ttu-id="ed95e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed95e-114">-DefaultProfile</span></span>
<span data-ttu-id="ed95e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed95e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed95e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed95e-116">-InputObject</span></span>
<span data-ttu-id="ed95e-117">Configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="ed95e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed95e-118">-Name</span></span>
<span data-ttu-id="ed95e-119">Nome di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="ed95e-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ed95e-120">-ParentName</span></span>
<span data-ttu-id="ed95e-121">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-121">The integration account name.</span></span>

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

### <span data-ttu-id="ed95e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed95e-122">-PassThru</span></span>
<span data-ttu-id="ed95e-123">Indica se il comando ha avuto esito positivo o meno.</span><span class="sxs-lookup"><span data-stu-id="ed95e-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="ed95e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed95e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed95e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed95e-125">The resource group name.</span></span>

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

### <span data-ttu-id="ed95e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed95e-126">-ResourceId</span></span>
<span data-ttu-id="ed95e-127">ID risorsa di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ed95e-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="ed95e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed95e-128">-Confirm</span></span>
<span data-ttu-id="ed95e-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed95e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed95e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed95e-130">-WhatIf</span></span>
<span data-ttu-id="ed95e-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed95e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed95e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed95e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed95e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed95e-133">CommonParameters</span></span>
<span data-ttu-id="ed95e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed95e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed95e-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed95e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed95e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed95e-136">INPUTS</span></span>

### <span data-ttu-id="ed95e-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed95e-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="ed95e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ed95e-138">System.String</span></span>

## <span data-ttu-id="ed95e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed95e-139">OUTPUTS</span></span>

### <span data-ttu-id="ed95e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed95e-140">System.Boolean</span></span>

## <span data-ttu-id="ed95e-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed95e-141">NOTES</span></span>

## <span data-ttu-id="ed95e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed95e-142">RELATED LINKS</span></span>
