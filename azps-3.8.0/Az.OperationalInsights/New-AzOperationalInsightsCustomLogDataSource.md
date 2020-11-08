---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018593"
---
# <span data-ttu-id="9af69-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="9af69-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="9af69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9af69-102">SYNOPSIS</span></span>
<span data-ttu-id="9af69-103">Definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="9af69-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="9af69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9af69-104">SYNTAX</span></span>

### <span data-ttu-id="9af69-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9af69-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af69-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9af69-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9af69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9af69-107">DESCRIPTION</span></span>
<span data-ttu-id="9af69-108">Il cmdlet **New-AzOperationalInsightsCustomLogDataSource** definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="9af69-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="9af69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9af69-109">EXAMPLES</span></span>

## <span data-ttu-id="9af69-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9af69-110">PARAMETERS</span></span>

### <span data-ttu-id="9af69-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="9af69-111">-CustomLogRawJson</span></span>
<span data-ttu-id="9af69-112">Specifica i criteri di raccolta personalizzati come stringa JSON (JavaScript Object Notation) non elaborata.</span><span class="sxs-lookup"><span data-stu-id="9af69-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af69-113">-DefaultProfile</span></span>
<span data-ttu-id="9af69-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9af69-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9af69-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9af69-115">-Force</span></span>
<span data-ttu-id="9af69-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9af69-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9af69-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9af69-117">-Name</span></span>
<span data-ttu-id="9af69-118">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="9af69-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af69-119">-ResourceGroupName</span></span>
<span data-ttu-id="9af69-120">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="9af69-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9af69-121">-Workspace</span></span>
<span data-ttu-id="9af69-122">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9af69-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9af69-123">-WorkspaceName</span></span>
<span data-ttu-id="9af69-124">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9af69-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9af69-125">-Confirm</span></span>
<span data-ttu-id="9af69-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9af69-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af69-127">-WhatIf</span></span>
<span data-ttu-id="9af69-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9af69-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af69-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9af69-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af69-130">CommonParameters</span></span>
<span data-ttu-id="9af69-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af69-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af69-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af69-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9af69-133">INPUTS</span></span>

### <span data-ttu-id="9af69-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9af69-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9af69-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9af69-135">System.String</span></span>

## <span data-ttu-id="9af69-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9af69-136">OUTPUTS</span></span>

### <span data-ttu-id="9af69-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9af69-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9af69-138">Note</span><span class="sxs-lookup"><span data-stu-id="9af69-138">NOTES</span></span>

## <span data-ttu-id="9af69-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9af69-139">RELATED LINKS</span></span>

[<span data-ttu-id="9af69-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="9af69-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="9af69-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="9af69-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


