---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486164"
---
# <span data-ttu-id="52dbc-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52dbc-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="52dbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="52dbc-103">Rimuovere un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="52dbc-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="52dbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52dbc-104">SYNTAX</span></span>

### <span data-ttu-id="52dbc-105">DataConnectorId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52dbc-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52dbc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52dbc-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52dbc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="52dbc-108">Il cmdlet **Remove-AzSentinelDataConnector** Elimina definitivamente un connettore di dati da un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="52dbc-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="52dbc-109">Puoi passare un oggetto **DataConnector** usando l'operatore pipeline o in alternativa puoi specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="52dbc-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="52dbc-110">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="52dbc-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="52dbc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52dbc-111">EXAMPLES</span></span>

### <span data-ttu-id="52dbc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52dbc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="52dbc-113">Questo comando rimuove il DataConnector dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="52dbc-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="52dbc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52dbc-114">PARAMETERS</span></span>

### <span data-ttu-id="52dbc-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="52dbc-115">-DataConnectorId</span></span>
<span data-ttu-id="52dbc-116">ID connettore dati.</span><span class="sxs-lookup"><span data-stu-id="52dbc-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="52dbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52dbc-117">-DefaultProfile</span></span>
<span data-ttu-id="52dbc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52dbc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52dbc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52dbc-119">-InputObject</span></span>
<span data-ttu-id="52dbc-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="52dbc-120">InputObject.</span></span>

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

### <span data-ttu-id="52dbc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52dbc-121">-PassThru</span></span>
<span data-ttu-id="52dbc-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="52dbc-122">PassThru</span></span>

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

### <span data-ttu-id="52dbc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52dbc-123">-ResourceGroupName</span></span>
<span data-ttu-id="52dbc-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52dbc-124">Resource group name.</span></span>

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

### <span data-ttu-id="52dbc-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52dbc-125">-WorkspaceName</span></span>
<span data-ttu-id="52dbc-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="52dbc-126">Workspace Name.</span></span>

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

### <span data-ttu-id="52dbc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52dbc-127">-Confirm</span></span>
<span data-ttu-id="52dbc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52dbc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52dbc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52dbc-129">-WhatIf</span></span>
<span data-ttu-id="52dbc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52dbc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52dbc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52dbc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52dbc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52dbc-132">CommonParameters</span></span>
<span data-ttu-id="52dbc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52dbc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52dbc-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52dbc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52dbc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52dbc-135">INPUTS</span></span>

### <span data-ttu-id="52dbc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="52dbc-136">System.String</span></span>
### <span data-ttu-id="52dbc-137">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52dbc-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="52dbc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52dbc-138">OUTPUTS</span></span>

### <span data-ttu-id="52dbc-139">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52dbc-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="52dbc-140">Note</span><span class="sxs-lookup"><span data-stu-id="52dbc-140">NOTES</span></span>

## <span data-ttu-id="52dbc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52dbc-141">RELATED LINKS</span></span>
