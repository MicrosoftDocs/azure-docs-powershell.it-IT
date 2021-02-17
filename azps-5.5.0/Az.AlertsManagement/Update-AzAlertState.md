---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205883"
---
# <span data-ttu-id="31810-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="31810-101">Update-AzAlertState</span></span>

## <span data-ttu-id="31810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31810-102">SYNOPSIS</span></span>
<span data-ttu-id="31810-103">Aggiorna lo stato di avviso</span><span class="sxs-lookup"><span data-stu-id="31810-103">Updates alert state</span></span>

## <span data-ttu-id="31810-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31810-104">SYNTAX</span></span>

### <span data-ttu-id="31810-105">ByAlertId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31810-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31810-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31810-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31810-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31810-107">DESCRIPTION</span></span>
<span data-ttu-id="31810-108">Il cmdlet **Update-AzAlertState** aggiorna lo stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="31810-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="31810-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31810-109">EXAMPLES</span></span>

### <span data-ttu-id="31810-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31810-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="31810-111">Questo cmdlet aggiorna lo stato dell'avviso in Chiuso.</span><span class="sxs-lookup"><span data-stu-id="31810-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="31810-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31810-112">PARAMETERS</span></span>

### <span data-ttu-id="31810-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="31810-113">-AlertId</span></span>
<span data-ttu-id="31810-114">Identificatore univoco dell'avviso/ID risorsa dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="31810-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="31810-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31810-115">-DefaultProfile</span></span>
<span data-ttu-id="31810-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31810-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31810-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31810-117">-InputObject</span></span>
<span data-ttu-id="31810-118">Oggetto di input dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="31810-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="31810-119">-State</span><span class="sxs-lookup"><span data-stu-id="31810-119">-State</span></span>
<span data-ttu-id="31810-120">Stato avviso aggiornato</span><span class="sxs-lookup"><span data-stu-id="31810-120">Updated Alert State</span></span>

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

### <span data-ttu-id="31810-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31810-121">-Confirm</span></span>
<span data-ttu-id="31810-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31810-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31810-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31810-123">-WhatIf</span></span>
<span data-ttu-id="31810-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31810-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31810-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31810-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31810-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31810-126">CommonParameters</span></span>
<span data-ttu-id="31810-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31810-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31810-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31810-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31810-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="31810-129">INPUTS</span></span>

### <span data-ttu-id="31810-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31810-130">None</span></span>

## <span data-ttu-id="31810-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31810-131">OUTPUTS</span></span>

### <span data-ttu-id="31810-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="31810-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="31810-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="31810-133">NOTES</span></span>

## <span data-ttu-id="31810-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31810-134">RELATED LINKS</span></span>
