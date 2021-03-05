---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 1ab5abc4af394647fd1438ed79cebb739daaca94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985472"
---
# <span data-ttu-id="363b9-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="363b9-101">Update-AzAlertState</span></span>

## <span data-ttu-id="363b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="363b9-102">SYNOPSIS</span></span>
<span data-ttu-id="363b9-103">Aggiorna lo stato di avviso</span><span class="sxs-lookup"><span data-stu-id="363b9-103">Updates alert state</span></span>

## <span data-ttu-id="363b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="363b9-104">SYNTAX</span></span>

### <span data-ttu-id="363b9-105">ByAlertId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="363b9-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="363b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="363b9-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="363b9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="363b9-107">DESCRIPTION</span></span>
<span data-ttu-id="363b9-108">Il cmdlet **Update-AzAlertState** aggiorna lo stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="363b9-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="363b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="363b9-109">EXAMPLES</span></span>

### <span data-ttu-id="363b9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="363b9-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="363b9-111">Questo cmdlet aggiorna lo stato dell'avviso in Chiuso.</span><span class="sxs-lookup"><span data-stu-id="363b9-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="363b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="363b9-112">PARAMETERS</span></span>

### <span data-ttu-id="363b9-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="363b9-113">-AlertId</span></span>
<span data-ttu-id="363b9-114">Identificatore univoco dell'avviso/ID risorsa dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="363b9-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="363b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363b9-115">-DefaultProfile</span></span>
<span data-ttu-id="363b9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="363b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="363b9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="363b9-117">-InputObject</span></span>
<span data-ttu-id="363b9-118">Oggetto di input dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="363b9-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="363b9-119">-State</span><span class="sxs-lookup"><span data-stu-id="363b9-119">-State</span></span>
<span data-ttu-id="363b9-120">Stato avviso aggiornato</span><span class="sxs-lookup"><span data-stu-id="363b9-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="363b9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="363b9-121">-Confirm</span></span>
<span data-ttu-id="363b9-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="363b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="363b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="363b9-123">-WhatIf</span></span>
<span data-ttu-id="363b9-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="363b9-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="363b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363b9-126">CommonParameters</span></span>
<span data-ttu-id="363b9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="363b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363b9-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="363b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363b9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="363b9-129">INPUTS</span></span>

### <span data-ttu-id="363b9-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="363b9-130">None</span></span>

## <span data-ttu-id="363b9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="363b9-131">OUTPUTS</span></span>

### <span data-ttu-id="363b9-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="363b9-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="363b9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="363b9-133">NOTES</span></span>

## <span data-ttu-id="363b9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="363b9-134">RELATED LINKS</span></span>
