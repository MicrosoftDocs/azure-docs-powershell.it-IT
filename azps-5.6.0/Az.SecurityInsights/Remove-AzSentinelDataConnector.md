---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978126"
---
# <span data-ttu-id="eefa2-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="eefa2-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="eefa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefa2-102">SYNOPSIS</span></span>
<span data-ttu-id="eefa2-103">Rimuovere un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="eefa2-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="eefa2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eefa2-104">SYNTAX</span></span>

### <span data-ttu-id="eefa2-105">DataConnectorId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eefa2-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefa2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eefa2-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefa2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eefa2-107">DESCRIPTION</span></span>
<span data-ttu-id="eefa2-108">Il cmdlet **Remove-AzSentinelDataConnector** elimina definitivamente un connettore di dati da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="eefa2-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="eefa2-109">È possibile passare un **oggetto DataConnector** usando l'operatore della pipeline oppure è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="eefa2-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="eefa2-110">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="eefa2-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="eefa2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eefa2-111">EXAMPLES</span></span>

### <span data-ttu-id="eefa2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eefa2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="eefa2-113">Questo comando rimuove DataConnector dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefa2-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="eefa2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefa2-114">PARAMETERS</span></span>

### <span data-ttu-id="eefa2-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="eefa2-115">-DataConnectorId</span></span>
<span data-ttu-id="eefa2-116">ID connettore dati.</span><span class="sxs-lookup"><span data-stu-id="eefa2-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefa2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefa2-117">-DefaultProfile</span></span>
<span data-ttu-id="eefa2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eefa2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefa2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eefa2-119">-InputObject</span></span>
<span data-ttu-id="eefa2-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="eefa2-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eefa2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eefa2-121">-PassThru</span></span>
<span data-ttu-id="eefa2-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="eefa2-122">PassThru</span></span>

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

### <span data-ttu-id="eefa2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefa2-123">-ResourceGroupName</span></span>
<span data-ttu-id="eefa2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eefa2-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefa2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eefa2-125">-WorkspaceName</span></span>
<span data-ttu-id="eefa2-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="eefa2-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefa2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eefa2-127">-Confirm</span></span>
<span data-ttu-id="eefa2-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefa2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefa2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefa2-129">-WhatIf</span></span>
<span data-ttu-id="eefa2-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefa2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefa2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefa2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefa2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefa2-132">CommonParameters</span></span>
<span data-ttu-id="eefa2-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefa2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefa2-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eefa2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefa2-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="eefa2-135">INPUTS</span></span>

### <span data-ttu-id="eefa2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eefa2-136">System.String</span></span>
### <span data-ttu-id="eefa2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="eefa2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="eefa2-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eefa2-138">OUTPUTS</span></span>

### <span data-ttu-id="eefa2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="eefa2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="eefa2-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="eefa2-140">NOTES</span></span>

## <span data-ttu-id="eefa2-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eefa2-141">RELATED LINKS</span></span>
