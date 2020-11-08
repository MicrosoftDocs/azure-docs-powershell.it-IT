---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199935"
---
# <span data-ttu-id="8de39-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="8de39-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="8de39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8de39-102">SYNOPSIS</span></span>

<span data-ttu-id="8de39-103">Sincronizza un database specificato nell'istanza specificata di Analysis Services server in tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8de39-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8de39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8de39-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8de39-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8de39-105">DESCRIPTION</span></span>

<span data-ttu-id="8de39-106">Il cmdlet Sync-AzAnalysisServicesInstance sincronizza un database specificato nell'istanza specificata di Analysis Services server per tutte le istanze di scalabilità delle query nell'ambiente attualmente connesso, come specificato in Add-AzAnalysisServicesAccount comando</span><span class="sxs-lookup"><span data-stu-id="8de39-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8de39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8de39-107">EXAMPLES</span></span>

### <span data-ttu-id="8de39-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8de39-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="8de39-109">Questo comando Sincronizza il database denominato SalesOrders nel server denominato ' Contoso ' nell'ambiente westus.asazure.windows.net a condizione che l'utente abbia effettuato l'accesso a questo ambiente usando il comando Add-AzAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="8de39-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="8de39-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8de39-110">PARAMETERS</span></span>

### <span data-ttu-id="8de39-111">-Database</span><span class="sxs-lookup"><span data-stu-id="8de39-111">-Database</span></span>

<span data-ttu-id="8de39-112">Identità del database da sincronizzare</span><span class="sxs-lookup"><span data-stu-id="8de39-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="8de39-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="8de39-113">-Instance</span></span>

<span data-ttu-id="8de39-114">Nome dell'istanza del server Analysis Services da riavviare</span><span class="sxs-lookup"><span data-stu-id="8de39-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="8de39-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de39-115">-PassThru</span></span>

<span data-ttu-id="8de39-116">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="8de39-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8de39-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8de39-117">-Confirm</span></span>
<span data-ttu-id="8de39-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de39-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de39-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de39-119">-WhatIf</span></span>
<span data-ttu-id="8de39-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8de39-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8de39-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8de39-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de39-122">CommonParameters</span></span>
<span data-ttu-id="8de39-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de39-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de39-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de39-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8de39-125">INPUTS</span></span>

### <span data-ttu-id="8de39-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8de39-126">System.String</span></span>

## <span data-ttu-id="8de39-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8de39-127">OUTPUTS</span></span>

### <span data-ttu-id="8de39-128">Microsoft. Azure. Commands. AnalysisServices. dataplane. Models. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="8de39-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="8de39-129">Note</span><span class="sxs-lookup"><span data-stu-id="8de39-129">NOTES</span></span>

<span data-ttu-id="8de39-130">Alias: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="8de39-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="8de39-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8de39-131">RELATED LINKS</span></span>