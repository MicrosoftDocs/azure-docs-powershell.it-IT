---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521869"
---
# <span data-ttu-id="e0aa9-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="e0aa9-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="e0aa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="e0aa9-103">Definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0aa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0aa9-104">SYNTAX</span></span>

### <span data-ttu-id="e0aa9-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0aa9-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0aa9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0aa9-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0aa9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0aa9-107">DESCRIPTION</span></span>
<span data-ttu-id="e0aa9-108">Il cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** definisce criteri di raccolta di log personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="e0aa9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0aa9-109">EXAMPLES</span></span>

## <span data-ttu-id="e0aa9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0aa9-110">PARAMETERS</span></span>

### <span data-ttu-id="e0aa9-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="e0aa9-111">-CustomLogRawJson</span></span>
<span data-ttu-id="e0aa9-112">Specifica i criteri di raccolta personalizzati come stringa JSON (JavaScript Object Notation) non elaborata.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0aa9-113">-DefaultProfile</span></span>
<span data-ttu-id="e0aa9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0aa9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e0aa9-115">-Force</span></span>
<span data-ttu-id="e0aa9-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0aa9-117">-Name</span></span>
<span data-ttu-id="e0aa9-118">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0aa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="e0aa9-120">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-121">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e0aa9-121">-Workspace</span></span>
<span data-ttu-id="e0aa9-122">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0aa9-123">-WorkspaceName</span></span>
<span data-ttu-id="e0aa9-124">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0aa9-125">-Confirm</span></span>
<span data-ttu-id="e0aa9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0aa9-127">-WhatIf</span></span>
<span data-ttu-id="e0aa9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0aa9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0aa9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0aa9-130">CommonParameters</span></span>
<span data-ttu-id="e0aa9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0aa9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0aa9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0aa9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0aa9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0aa9-133">INPUTS</span></span>

### <span data-ttu-id="e0aa9-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0aa9-134">PSWorkspace</span></span>
<span data-ttu-id="e0aa9-135">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e0aa9-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e0aa9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0aa9-136">OUTPUTS</span></span>

### <span data-ttu-id="e0aa9-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e0aa9-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e0aa9-138">Note</span><span class="sxs-lookup"><span data-stu-id="e0aa9-138">NOTES</span></span>

## <span data-ttu-id="e0aa9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0aa9-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0aa9-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e0aa9-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="e0aa9-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e0aa9-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


