---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: b364833be9219d778bc9d204f7e1a61a1667fe1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687286"
---
# <span data-ttu-id="11bd1-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="11bd1-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="11bd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="11bd1-103">Definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="11bd1-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11bd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11bd1-104">SYNTAX</span></span>

### <span data-ttu-id="11bd1-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11bd1-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11bd1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11bd1-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11bd1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="11bd1-108">Il cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="11bd1-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="11bd1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11bd1-109">EXAMPLES</span></span>

## <span data-ttu-id="11bd1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11bd1-110">PARAMETERS</span></span>

### <span data-ttu-id="11bd1-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="11bd1-111">-CustomLogRawJson</span></span>
<span data-ttu-id="11bd1-112">Specifica i criteri di raccolta personalizzati come stringa JSON (JavaScript Object Notation) non elaborata.</span><span class="sxs-lookup"><span data-stu-id="11bd1-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="11bd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bd1-113">-DefaultProfile</span></span>
<span data-ttu-id="11bd1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="11bd1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bd1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="11bd1-115">-Force</span></span>
<span data-ttu-id="11bd1-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="11bd1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11bd1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="11bd1-117">-Name</span></span>
<span data-ttu-id="11bd1-118">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="11bd1-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="11bd1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bd1-119">-ResourceGroupName</span></span>
<span data-ttu-id="11bd1-120">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="11bd1-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="11bd1-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="11bd1-121">-Workspace</span></span>
<span data-ttu-id="11bd1-122">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bd1-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="11bd1-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11bd1-123">-WorkspaceName</span></span>
<span data-ttu-id="11bd1-124">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bd1-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="11bd1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11bd1-125">-Confirm</span></span>
<span data-ttu-id="11bd1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bd1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bd1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11bd1-127">-WhatIf</span></span>
<span data-ttu-id="11bd1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11bd1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bd1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11bd1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bd1-130">CommonParameters</span></span>
<span data-ttu-id="11bd1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bd1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11bd1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bd1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11bd1-133">INPUTS</span></span>

### <span data-ttu-id="11bd1-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="11bd1-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="11bd1-135">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11bd1-135">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="11bd1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="11bd1-136">System.String</span></span>

## <span data-ttu-id="11bd1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11bd1-137">OUTPUTS</span></span>

### <span data-ttu-id="11bd1-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="11bd1-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="11bd1-139">Note</span><span class="sxs-lookup"><span data-stu-id="11bd1-139">NOTES</span></span>

## <span data-ttu-id="11bd1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11bd1-140">RELATED LINKS</span></span>

[<span data-ttu-id="11bd1-141">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="11bd1-141">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="11bd1-142">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="11bd1-142">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


