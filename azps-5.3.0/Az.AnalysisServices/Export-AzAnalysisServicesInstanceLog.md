---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479092"
---
# <span data-ttu-id="f490a-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="f490a-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="f490a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f490a-102">SYNOPSIS</span></span>
<span data-ttu-id="f490a-103">Esporta un log da un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato nel comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f490a-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="f490a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f490a-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f490a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f490a-105">DESCRIPTION</span></span>
<span data-ttu-id="f490a-106">Il cmdlet Export-AzAnalysisServicesInstance Esporta il log da un'istanza di Azure Analysis Services server a file</span><span class="sxs-lookup"><span data-stu-id="f490a-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="f490a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f490a-107">EXAMPLES</span></span>

### <span data-ttu-id="f490a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f490a-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="f490a-109">Questo comando esporterà il log dal server "TestServer" nell'ambiente specificato nel comando Add-AzAnalysisServicesAccount e lo salverà in file specificato in OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="f490a-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="f490a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f490a-110">PARAMETERS</span></span>

### <span data-ttu-id="f490a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f490a-111">-Force</span></span>
<span data-ttu-id="f490a-112">Sovrascrivere il file se esiste senza chiedere</span><span class="sxs-lookup"><span data-stu-id="f490a-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="f490a-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="f490a-113">-Instance</span></span>
<span data-ttu-id="f490a-114">Nome dell'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f490a-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="f490a-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f490a-115">-OutputPath</span></span>
<span data-ttu-id="f490a-116">Percorso di output del file per esportare il log</span><span class="sxs-lookup"><span data-stu-id="f490a-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="f490a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f490a-117">-PassThru</span></span>
<span data-ttu-id="f490a-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f490a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f490a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f490a-119">-Confirm</span></span>
<span data-ttu-id="f490a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f490a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f490a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f490a-121">-WhatIf</span></span>
<span data-ttu-id="f490a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f490a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f490a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f490a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f490a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f490a-124">CommonParameters</span></span>
<span data-ttu-id="f490a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f490a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f490a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f490a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f490a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f490a-127">INPUTS</span></span>

### <span data-ttu-id="f490a-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f490a-128">None</span></span>

## <span data-ttu-id="f490a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f490a-129">OUTPUTS</span></span>

### <span data-ttu-id="f490a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f490a-130">System.Void</span></span>

## <span data-ttu-id="f490a-131">Note</span><span class="sxs-lookup"><span data-stu-id="f490a-131">NOTES</span></span>
<span data-ttu-id="f490a-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="f490a-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="f490a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f490a-133">RELATED LINKS</span></span>
