---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959229"
---
# <span data-ttu-id="4bbed-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="4bbed-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="4bbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbed-102">SYNOPSIS</span></span>

<span data-ttu-id="4bbed-103">Sincronizza un database specificato nell'istanza specificata del server analysis services con tutte le istanze di scalabilità della query nell'ambiente attualmente connesso come specificato nel comando Add-AzAnalysisServicesAccount></span><span class="sxs-lookup"><span data-stu-id="4bbed-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="4bbed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bbed-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bbed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4bbed-105">DESCRIPTION</span></span>

<span data-ttu-id="4bbed-106">Il cmdlet Sync-AzAnalysisServicesInstance sincronizza un database specificato nell'istanza specificata del server Analysis Services con tutte le istanze di scalabilità della query nell'ambiente attualmente connesso come specificato nel comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bbed-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="4bbed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bbed-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbed-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bbed-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="4bbed-109">Questo comando sincronirà il database denominato SalesOrders nel server denominato "contoso" nell'ambiente westus.asazure.windows.net a condizione che l'utente abbia eseguito l'accesso a questo ambiente usando Add-AzAnalysisServicesAccount comando.</span><span class="sxs-lookup"><span data-stu-id="4bbed-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="4bbed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bbed-110">PARAMETERS</span></span>

### <span data-ttu-id="4bbed-111">-Database</span><span class="sxs-lookup"><span data-stu-id="4bbed-111">-Database</span></span>

<span data-ttu-id="4bbed-112">Identità del database da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="4bbed-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbed-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="4bbed-113">-Instance</span></span>

<span data-ttu-id="4bbed-114">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="4bbed-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbed-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bbed-115">-PassThru</span></span>

<span data-ttu-id="4bbed-116">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4bbed-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4bbed-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bbed-117">-Confirm</span></span>
<span data-ttu-id="4bbed-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bbed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bbed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbed-119">-WhatIf</span></span>
<span data-ttu-id="4bbed-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bbed-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bbed-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bbed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bbed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbed-122">CommonParameters</span></span>
<span data-ttu-id="4bbed-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bbed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbed-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbed-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4bbed-125">INPUTS</span></span>

### <span data-ttu-id="4bbed-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4bbed-126">System.String</span></span>

## <span data-ttu-id="4bbed-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bbed-127">OUTPUTS</span></span>

### <span data-ttu-id="4bbed-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="4bbed-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="4bbed-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4bbed-129">NOTES</span></span>

<span data-ttu-id="4bbed-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="4bbed-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="4bbed-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bbed-131">RELATED LINKS</span></span>
